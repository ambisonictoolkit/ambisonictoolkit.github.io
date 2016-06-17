---
layout: post
title:  ATK Kernels v.1.2.1 released
author: Joseph Anderson
date:   2016-06-17 12:30:00 +0800
categories: releases
---


ATK Kernels v.1.2.1 package is now available for download. This version includes
a number of additions and corrections. The following sample rates are now
supported by _all_ encoders and decoders:

*  44100, 48000, 88200, 96000, 176400, 192000

Of particular interest, binaural decoders generated from _measured_ HRTFs,
the [CIPIC](http://interface.cipic.ucdavis.edu/sound/hrtf.html) &
[Listen](http://recherche.ircam.fr/equipes/salles/listen/) sets, now fully
support _all_ of the above sample rates. Additionally, you'll see we've updated
the
[README](https://github.com/ambisonictoolkit/atk-kernels/blob/v1.2.1/README.md)
to include more details as to how the ATK's kernels are designed and what they
do. You'll note _we've_ done lot's of cool Ambisonic stuff so _you_ can do cool
Ambisonic stuff, too!

---
#### How to upgrade? ####

If you're an [ATK for SuperCollider](/download/supercollider/) user, just
follow the instructions [here](/download/kernels/). You'll be replacing your
current `ATK/kernels` folder with the new one.

What about the [ATK for Reaper](/download/reaper/) folks? The new version will
soon be appearing [here](/download/reaper/). If you're adventurous (and over
excited?), you _can_ replace your current `ATK/kernels` folder by hand. On OSX
it is found at: `~/Library/Application Support/ATK/kernels`

If you've installed both [ATK for SuperCollider](/download/supercollider/) &
[ATK for Reaper](/download/reaper/), with this release updating
[ATK for SuperCollider](/download/supercollider/) should do the trick!
