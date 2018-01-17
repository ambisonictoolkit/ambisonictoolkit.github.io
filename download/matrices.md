---
layout: page
title: Matrices<br/><small>A set of matrix files for matrix encoders and decoders</small>
permalink: /download/matrices/
---

<p>&nbsp;</p>

<p class="text-center">
  <a href="https://github.com/ambisonictoolkit/atk-matrices/releases/latest" class="btn btn-success btn-lg">Download Matrices</a>
</p>

<p>&nbsp;</p>

<div class="alert alert-success">

  <h2>Using Matrices with Reaper</h2>

  <p>The Matrices are already included as part of the <a href="/download/reaper/">ATK for Reaper</a> install, and there is no need to download and install the matrices seperately.</p>

</div>

&nbsp;

<div class="alert alert-info">

<h2>Using Matrices with SuperCollider</h2>

<p>Install <a href="/download/supercollider/">ATK for SuperCollider</a>. Launch SuperCollider3, and run the following code:</p>

<p>&nbsp;</p>

<pre>
ATK Matrix Installation
(
// Create ATK support directory
// Place unzipped matrices in the directory opened  

Atk.createUserSupportDir;
Atk.openUserSupportDir;
)
</pre>

<p>&nbsp;</p>

<p>If ATK for SuperCollider has been correctly installed, the above code will open the ATK's user support directory. Place the downloaded matrices here.</p>

</div>

&nbsp;

### License

<a rel="license" href="http://creativecommons.org/licenses/by-sa/3.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/3.0/88x31.png" /></a><br />The Ambisonic Toolkit Matrices package is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/3.0/">Creative Commons Attribution-ShareAlike 3.0 Unported License</a>.

Copyright the [Ambisonic Toolkit](http://ambisonictoolkit.net) Community and Joseph Anderson, 2017.
