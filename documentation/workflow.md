---
layout: page
title: Introduction<br/><small>The Ambisonic Toolkit Workflow</small>
permalink: /documentation/workflow/
---


<p class="lead">ATK separates the task of production work with Ambisonics into three distinct elements.</p>

<figure class="figure">
  <img src="/assets/images/documentation/workflow/atk-network.svg" alt="alt text" title="The Ambisonic Toolkit workflow" class="img-responsive center-block" style="width: 100%; max-width: 712px; padding-top: 2em; padding-bottom: 1em" />
  <figcaption class="figure-caption text-center">The Ambisonic Toolkit paradigmatic workflow.</figcaption>
</figure>

&nbsp;

&nbsp;

<dl class="dl-horizontal">
  <dt>Author</dt>
  <dd>Capture or synthesise an Ambisonic soundfield.</dd>
  <dt>Image</dt>
  <dd>Spatially filter an Ambisonic soundfield.</dd>
  <dt>Monitor</dt>
  <dd>Playback or render an Ambisonic soundfield.</dd>
</dl>

In its most simple form, Ambisonics can be regarded as splitting the panning law into two separate parts: encoding (Authoring) and decoding (Monitoring), where final panning (decoding) is deferred to an actual loudspeaker array at the time of audition. The ATK considers the Imaging (transforming) of a soundfield to be a critical step; this is where the artist shapes and processes the soundfield in a coherent way which isn’t easily available via the other models for working with spatial sound.

Many publicly distributed implementations of Ambisonics provide only encoding and decoding. While giving flexibility regarding final playback, failing to include transformers misses out the concept of imaging and fails to capitalise on the advantages of the sound-field sound-image paradigm intrinsic to Ambisonics.

### What's the difference?

The real power in working with <a href="https://en.wikipedia.org/wiki/Ambisonics" target="_blank">Ambisonic</a> over other multichannel surround sound techniques is that rather than being restricted to a sound-scene based paradigm (where the artist is presented with tools designed to build up a ‘sound scene’) Ambisonics supports a soundfield-kernel model. Here we construct a soundfield in the abstract, and can then shape it as desired. The result may be shaped into a ‘sound scene’, or perceived this way &ndash; but a soundfield-kernel approach gives much greater flexibility, and directly supports the realisation of more abstract outcomes. We regard this model as idiomatic for Ambisonics.

Along with powerful soundfield transforms &ndash; the spatial filtering tools enabling soundfield-kernel reshaping &ndash; the ATK provides a comprehensive set of Ambisonic encoders (including pseudo-inverse) and decoders (<a href="https://en.wikipedia.org/wiki/5.1" target="_blank">5.1</a>, <a href="https://en.wikipedia.org/wiki/Binaural_recording" target="_blank">binaural</a>, <a href="https://en.wikipedia.org/wiki/UHJ_format" target="_blank">UHJ</a>, full-3D) allowing users to thoroughly leverage the power of the Ambisonic technique.