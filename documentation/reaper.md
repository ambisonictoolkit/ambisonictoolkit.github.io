---
layout: page
title: ATK for Reaper
permalink: /documentation/reaper/
---

<p class="lead">ATK for Reaper is a set of plugins for the <a href="http://reaper.fm">Reaper DAW</a>. Using the <abbr title="ReaJS plugin is part of the ReaPlugs VST FX Suite.">ReaJS plugin</abbr> ATK for Reaper can also be used with other DAWs on Windows that support VST plugins.</p>

<p class="text-center">
  <img src="/assets/images/documentation/reaper/plugins.png" alt="alt text" title="ImagingTransform Plugins" class="img-responsive center-block" />
</p>

&nbsp;

The plugins are developed in the [JS FX](http://reaper.fm/sdk/js/js.php) scripting language, and work with all platforms and processors supported by Reaper. Several of the plugins, most notably the Transforms, are provided with graphical user interfaces that help visualise the effect of the transform.


## Overview of plugins


<h3 class="page-header">Encoders</h3>

<h4 class="page-header">Mono signals</h4>

<dl class="dl-horizontal">
  <dt>Omni</dt>
  <dd>Encodes a mono signal as an omnidirectional soundfield.</dd>

  <dt>Planewave</dt>
  <dd>Provides classic encoding of a mono source as a planewave, where the arrival direction (azimuth and elevation) can be set.</dd>

  <dt>Spread</dt>
  <dd>Encodes a monophonic signal by smoothly rotating the signal across the soundfield by frequency.</dd>

  <dt>Diffuse</dt>
  <dd>Randomises the phase of the incoming monophonic signal to create a diffuse field.</dd>

  <dt>PseudoInverse</dt>
  <dd>Provides a great deal of flexibility, and can be used with both microphone arrays and synthetic signals. In the absence of a Soundfield microphone, this encoding technique gives the opportunity to deploy real-world microphone arrays (omni, cardioid, etc.) to capture natural soundfields. ZoomH2 adapts PseudoInverse for this popular portable recorder. <span class="bg-danger">Not yet implemented.</span> </dd>

</dl>

<h4 class="page-header">Stereo signals</h4>

<dl class="dl-horizontal">
  <dt>Stereo</dt>
  <dd>The Stereo plugin encodes stereo left and right channels as two planewaves coming from left and right; the angular spread between the two waves is parameterised.</dd>

  <dt>SuperStereo</dt>
  <dd>SuperStereo is the classic ‘super stereo’ method for encoding stereophonic signals.</dd>

  <dt>UHJ</dt>
  <dd>The UHJ encoder offers access to numerous published recordings for periphonic (2D) audition.
</dd>
</dl>

<h4 class="page-header">Multichannel signals</h4>

<dl class="dl-horizontal">
  <dt>Planewave transcoders</dt>
  <dd>Planewave transcoders are provided for a number of fixed-channel distribution formats: Quad, 5.0 and 7.0 for the standard ITU layouts, and Pantophonic for 2D and Periphonic for 3D arrays. <span class="bg-danger">Periphonic remains to be implemented.</span></dd>

  <dt>AtoB</dt>
  <dd>Provides a powerful method for constructing full, complex soundfields via A-format encoding. The user supplies four separate but related signals to be distributed equally throughout the three dimensions of the soundfield. These signals may either be synthesised or captured by microphones.</dd>
</dl>



<h3 class="page-header">Transformers</h3>

<h4 class="page-header">Imaging transforms</h4>


<dl class="dl-horizontal">
  <dt>Direct</dt>
  <dd>Adjusts the directivity of an FOA soundfield across the origin, functioning as a spatial low-pass filter; with an increasing degree of transformation, the soundfield becomes less directional, eventually becoming omnipresent.</dd>

  <dt>DirectO</dt>
  <dd>Adjusts the sound-field directivity across a plane specified by the user.</dd>

  <dt>FocusPressPushZoom</dt>
  <dd>Unified interface to four different spatial transforms. Focus and Zoom are dominance related transforms and can be described as ‘emphasising’ elements in the direction of interest. Press and Push differs, and rather than emphasising elements in a target direction, all are ‘pressed’ or ‘pushed’ towards the direction of interest. With increasing spatial transform all four transforms collapse the soundfield to a planewave arriving from the direction of interest specified by azimuth and elevation.
  </dd>

  <dt>Dominance</dt>
  <dd>Increases the gain of elements in the direction of interest while decreasing gain of elements in the opposite direction.</dd>

  <dt>Mirror</dt>
  <dd> Mirrors the soundfield across an arbitrary plane.</dd>

  <dt>MirrorO</dt>
  <dd>Mirrors the soundfield through the origin.</dd>

  <dt>RotateTiltTumble</dt>
  <dd>Multi-axes FOA rotations.</dd>
</dl>

<h4 class="page-header">Near-field effects</h4>

<dl class="dl-horizontal">
  <dt>Proximity</dt>
  <dd>Introduces the proximity effect to encoded signals.</dd>

  <dt>Nearfield</dt>
  <dd>Reduction or removal of the proximity effect from encoded signals.</dd>
</dl>


<h3 class="page-header">Decoders</h3>

<h4 class="page-header">Mono decoder</h4>

<dl class="dl-horizontal">
  <dt>Mono</dt>
  <dd>This virtual microphone decoder returns a single channel, and can be used to ‘listen in’ to the soundfield at the specified azimuth and elevation.</dd>
</dl>

<h4 class="page-header">Stereo decoders</h4>

<dl class="dl-horizontal">
  <dt>Stereo</dt>
  <dd>Returns a pair of virtual microphones.</dd>

  <dt>UHJ</dt>
  <dd>While the virtual microphone stereophonic decoder is very easy and convenient, for production work we advise using the UHJ decoder.</dd>
</dl>

<h4 class="page-header">Multichannel decoders</h4>

<dl class="dl-horizontal">
  <dt>Quad</dt>
  <dd>Optimised quadraphonic decoder with variable loudspeaker angle.</dd>

  <dt>5_0</dt>
  <dd>Uses Bruce Wiggins optimised ITU 5.0 decoders.</dd>

  <dt>Pantophonic2D</dt>
  <dd>A regular 2D polygon decoder.</dd>

  <dt>Periphonic</dt>
  <dd>A regular cylindrical decoder for 3D dual ring. <span class="bg-danger">Not yet implemented.</span> </dd>

  <dt>Diametric</dt>
  <dd>Gerzon’s classic decoder suit-able for varied periphonic and pantophonic loudspeaker arrays. <span class="bg-danger">Not yet implemented.</span> </dd>

  <dt>BtoA</dt>
  <dd>Decodes to to A-format. Can be used with AtoB and intermittent sound effects for sound design.</dd>

</dl>

<h4 class="page-header">Binaural decoder</h4>

<dl class="dl-horizontal">
  <dt>Binaural</dt>
  <dd>For headphone listening.</dd>
</dl>

<h3 class="page-header">Utilities</h3>

<dl class="dl-horizontal">
  <dt>4channels</dt>
  <dd>Extract 4 channel A- or B-format signal from multichannel recording.</dd>

  <dt>MuteSoloChannels</dt>
  <dd>Mute or solo individual channels of a four-channel track.</dd>
</dl>
