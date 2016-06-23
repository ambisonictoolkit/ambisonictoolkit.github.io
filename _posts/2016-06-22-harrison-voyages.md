---
layout: post
title:  Jonty Harrison's Voyages - ATK in action!
author: Joseph Anderson
date:   2016-06-22 15:30:00 +0800
categories: publications
---

<img src="/assets/images/2016-06-22-harrison-voyages/imed_16139.jpg" alt="alt text" title="Harrison-Voyages" class="img-responsive center-block" style="width: 100%; max-width: 600px; padding-top: 2em; padding-bottom: 1em" />

Jonty Harrison's latest CD,
[_Voyages_](http://www.electrocd.com/en/cat/imed_16139/), is now out. The
liner notes include a very
[brief note](http://www.electrocd.com/en/cat/imed_16139/notices/) describing how
this all came about and the involvement of the
[Ambisonic Toolkit](http://www.ambisonictoolkit.net/). The big question being,
"How to successfully 'down-mix' Harrison's (very-)multi-channel _Espaces cachés_
and _Going / Places_ to two channel stereo for CD release?" You know the answer
to this one: Use the
[ATK](http://www.ambisonictoolkit.net/)!


----

##### Some (Spatial) problems and (Spatial) solutions #####

The big problem: _Espaces cachés_ and _Going / Places_ are composed for large
loudspeaker arrays. (32 channels!) That's great if you've got a big room like a
concert hall to fill. But what about squeezing down to stereo?

Sensibly, the speakers can be be grouped into 'spatial stems' according to
their role in the pieces. E.g., of the 32 channels the array for
_Espaces cachés_, there are three 8 channel sub-groups: _distant_, _main_,
and _close_. In concert, the speakers for each of these sub-groups are placed in
the actual space accordingly. For the CD mix, we've got to somehow reproduce
this impression. But, just modeling the space (via designed or measured [RIRs](https://www.google.com/webhp?sourceid=chrome-instant&ion=1&espv=2&ie=UTF-8#q=room%20impulse%20response))
isn't going to do the right thing. That would end up sounding like 'adding
reverb' to the mix... not good!

The answer, of course, is to model the _spatial impression_, instead. For each
'spatial stem', we apply a different spatial filter set. The processing for the
above sub-groups can be summarized as:

*  _distant_: diffusion filtering
*  _main_: mid-field proximity filtering
*  _close_: near-field proximity filtering

Details are slightly more complicated, of course, but the idea is to use the
ATK's spatial filtering / processing to express the intended role of each
spatial stem. If we've got it right, we _should_ hear the layering intended by
the composer in the UHJ stereo mix. (Yeah... we got it right!)

---

#### How to Listen? ####

By design,
[Ambisonic UHJ Stereo](https://en.wikipedia.org/wiki/Ambisonic_UHJ_format) is
[stereo](https://en.wikipedia.org/wiki/Stereophonic_sound) compatible. Listening
over your own stereo system, it'll sound great. (This is one of the aspects of
working with Ambisonics I find so convenient, auto-magic stereo down-mix.) But
what about hearing Harrison's
[_Voyages_](http://www.electrocd.com/en/cat/imed_16139/) in full _surround-y
gloriousness_?

If you haven't done so already, follow the installation instructions for
[ATK for SuperCollider](/download/supercollider/) and / or
[ATK for Reaper](/download/reaper/). You'll then need to set up a signal chain
where you:

1. _Encode_: from UHJ Stereo to B-format
2. _Decode_: from B-format to _your favorite loudspeaker array_

If you've got quad, use the
[quad decoder](http://doc.sccode.org/Classes/FoaDecoderMatrix.html#*newQuad).
If you've got 5.0, use the
[5.0 decoder](http://doc.sccode.org/Classes/FoaDecoderMatrix.html#*new5_0).
If you've got a cube of eight speakers, use the
[periphonic decoder](http://doc.sccode.org/Classes/FoaDecoderMatrix.html#*newPeri).
If you've got headphones (who doesn't), try the
[binaural decoder](http://doc.sccode.org/Classes/FoaDecoderKernel.html#*newSpherical).
You get the picture.

Here's a _very_ simple example from the
[Help](http://doc.sccode.org/Guides/ATK-SynthDef-Examples.html) for
[ATK for SuperCollider](https://github.com/ambisonictoolkit/atk-sc3). You
won't exactly want to do it this way because the below code loads the complete
file into memory. Instead, use
[`DiskIn.ar`](http://doc.sccode.org/Classes/DiskIn.html) to stream in audio
from a file.

```
// encoding a UHJ file to B-format, then decoding through an HRTF decoder
(
var cond;
s.boot;
cond = Condition.new;
s.waitForBoot({
    Routine.run({
        ~encoder = FoaEncoderKernel.newUHJ;
        ~decoder = FoaDecoderKernel.newListen(1013);
        ~sndbuf = Buffer.read(s, Atk.userSoundsDir ++ "/uhj/Palestrina-O_Bone.wav");
        s.sync(cond);
        SynthDef(\kernelEncodeDecode, {arg buffer;
            var out, src, encode;
            src = PlayBuf.ar(2, buffer);
            encode = FoaEncode.ar(src, ~encoder);
            out = FoaDecode.ar(encode, ~decoder);
            Out.ar(0, out);
        }).add;
        s.sync(cond);
        Synth(\kernelEncodeDecode, [\buffer, ~sndbuf]);
        // press command period when done
        CmdPeriod.add({~encoder.free; ~decoder.free; ~sndbuf.free});
    })
})
)
```

---
As a side note, you'll be interested to hear that all the processing was done with the
_vapour-ware_ HOA version of the ATK. (We should really call it the
_super secret_ development version.) The mix was made in NFC-HOA5.
