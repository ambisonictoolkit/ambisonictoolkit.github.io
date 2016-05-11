---
layout: page
title: Kernels<br/><small>A set of impulse response files used for convolution-based encoders and decoders</small>
permalink: /download/kernels/
---

<p>&nbsp;</p>

<p class="text-center">
  <a href="https://github.com/ambisonictoolkit/atk-kernels/releases/latest" class="btn btn-success btn-lg">Download Kernels</a>
</p>

<p>&nbsp;</p>

<div class="alert alert-success">

  <h2>Using Kernels with Reaper</h2>

  <p>The Kernels are already included as part of the <a href="/download/reaper/">ATK for Reaper</a> install, and there is no need to download and install the kernels seperately.</p>

</div>

&nbsp;

<div class="alert alert-info">

<h2>Using Kernels with SuperCollider</h2>

<p>Install <a href="/download/supercollider/">ATK for SuperCollider</a>. Launch SuperCollider3, and run the following code:</p>

<p>&nbsp;</p>

<pre>
ATK Kernel Installation
(
// Create ATK support directory
// Place unzipped kernels in the directory opened  

Atk.createUserSupportDir;
Atk.openUserSupportDir;
)
</pre>

<p>&nbsp;</p>

<p>If ATK for SuperCollider has been correctly installed, the above code will open the ATK's user support directory. Place the downloaded kernels here.</p>

</div>

&nbsp;

### License

<a rel="license" href="http://creativecommons.org/licenses/by-sa/3.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/3.0/88x31.png" /></a><br />The Ambisonic Toolkit Kernels package is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/3.0/">Creative Commons Attribution-ShareAlike 3.0 Unported License</a>.

Copyright the [Ambisonic Toolkit](http://ambisonictoolkit.net) Community and Joseph Anderson, 2011.
