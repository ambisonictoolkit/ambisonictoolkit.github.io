---
layout: post
title:  BEAST FEAST Demo Reaper Project
author: Trond Lossius
date:   2016-05-03 13:00:00 +0100
categories: zoom
---


<img src="/assets/images/2016-05-03-beast-feast-demo-project/demo-project.png" alt="alt text" title="ATK Reaper demo project" class="img-responsive center-block" style="width: 100%; max-width: 600px; padding-top: 2em; padding-bottom: 1em" />

Thanks for the positive feedback to the presentation of ATK for Reaper at [BEAST: FEaST 2016](http://www.beast.bham.ac.uk/beast-feast-2016/) last weekend. lso, a general thanks to Scott and everyone else that helped organise the festival!

As promised, the Reaper project used during the presentation can now be [downloaded here](https://db.tt/g1D81Kxg).

<!--more-->

This Reaper project is a demo of the Ambisonic Toolkit plugins, with each track demoing different aspects of the toolkit. It uses the [standard sound files that we provide for ATK demo purposes](http://www.ambisonictoolkit.net/download/recordings/). Additionally the example project makes use of some other 3rd party plugins:

* [Matthias Kronlachner MCFS plugins](https://www.matthiaskronlachner.com/?p=1910)
* [Michal Norris AudioUnit plugins (Mac only)](http://www.michaelnorris.info/software/soundmagic-spectral)
* [Blue Ripple Harpex TOA Upcoder and Rapture 3D Advanced](http://www.blueripplesound.com/product-listings/pro-audio)
* [Harpex plugin](https://harpex.net/)

Here is some information on the various tracks in the project:

<dl class="dl-horizontal">
  <dt>Master track</dt>
  <dd>
    Decoding takes place here. It is set up to pass signals to a maximum of 24 channels, in accordance with the BEAST Doom configuration: Channesl 1-20 and 33-36.
    Depending on your listening setup, enable the apropriate plugin:
    <ul>
      <li>Binaural : Headphone listening</li>
      <li>Stereo : Stereo speakers</li>
      <li>UHJ Stereo : An alternative stereo decoders, often gives better results</li>
      <li>Quadrophonics : Four speakers - This plugin is set up for the BEAST Doom currently, and use the speaker pairs 3-4 and 5-6 in the setup. This is controlled by routing matrix for the plugin.</li>
      <li>Pantophonic 2D : Set to use 12 spakers - the full horisontal rig of the BEAST Doom.</li>
      <li>The last possibility is to upcode FOA to TOA using TOA Harpex, and then decode using TOA Decoder. These two plugins are not part of ATK, but are distributed by Blue Ripple Audio.</li>
    </ul>
  </dd>

  <dt>Harpex Monitor Track</dt>
  <dd>This track uses the Haprex plugin (not part of ATK) for visual display of source locations. Sound from this track is not passed on to the master track.
</dd>

  <dt>B-format Mix Track</dt>
  <dd>This folder track collects 4-channel audio from all subsequent tracks.</dd>

  <dt>B-format Transforms</dt>
  <dd>Uses a B-format recording as sound source. This track can be used to explore the various ATK Transforms.</dd>

  <dt>A-format FX Chain</dt>
  <dd>When FX-processing B-format signals, there is a risk of introducing phase distortions between the channels that may severely alter the spatial image. When doing non-linear FX processing, the trick is to first convert B-format to A-format, do the processing on A-format, and then re-encode to B-format. This track illustrates the process using a Michal Norris AudioUnit plugin (Mac only). Two stereo effects are used. One process channel 1-2 and the other is processing 3-4. This is controlled using the plugin channel routing matrix.</dd>
  
  <dt>Mono Encoding</dt>
  <dd>Can be used to test the various mono encoders. Please make sure that you are only using one at a time. Several of the encoders (omni, spread, diffuse) may need subsequent spatial transforms in order to make the resulting sound field less all-encompassing. If you have a license for the Harpex plugin and you want to study the spatial distribution of frequencies when using the Spread and Diffuse plugins, you can activate the noise plugin, in order to visualize the spatial encoding of a spectrally rich signal. <span class="bg-danger">If you do so, please make sure to bring the volumes down first, to protect ears and speakers.</span></dd>
  
  <dt>Stereo Encoding</dt>
  <dd>Can be used to test the two stereo encoders. Subsequent rotation, tilt and tumble may be needed to get the directions you want.</dd>
  
  <dt>UHJ Encoding</dt>
  <dd>If you have a stereo recording that is released as a UHJ decoding of an ambisonic recording, you can re-encode it using the UHJ encoder. Recordings released by the classical Nimbus record label are all UHJ recordings.</dd>
  
</dl>


