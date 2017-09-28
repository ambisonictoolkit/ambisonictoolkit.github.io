---
layout: page
title: Download ATK for SuperCollider 3<br/><small>An extension library for the SuperCollider programming language</small>
permalink: /download/supercollider/
---

&nbsp;

<div class="alert alert-info">

<h2>Distributed via the <a href="https://github.com/ambisonictoolkit/atk-sc3" target="_blank">atk-sc3 Quark</a> & the <a href="https://github.com/supercollider/sc3-plugins" target="_blank">sc3-plugins</a> project.</h2>


<h3>atk-sc3 Quark</h3>

<p>The ATK for <a href="http://supercollider.github.io" target="_blank">SuperCollider3</a>'s classes,
extension methods and documentation are distributed via the
<a href="https://github.com/ambisonictoolkit/atk-sc3" target="_blank">atk-sc3 Quark</a>. Start by reviewing
the Quark installation instructions
<a href="https://github.com/supercollider-quarks/quarks#installing" target="_blank">found here</a>. See
also <a href="http://doc.sccode.org/Guides/UsingQuarks.html" target="_blank">Using Quarks</a>.</p>


<p>With <a href="https://git-scm.com/" target="_blank">git</a> installed, you can easily install the
<a href="https://github.com/ambisonictoolkit/atk-sc3" target="_blank">atk-sc3 Quark</a> directly by
running the following line of code in SuperCollider:</p>

&nbsp;

<pre>
Quarks.install("https://github.com/ambisonictoolkit/atk-sc3.git");
</pre>


<h3>sc3-plugins</h3>

<p>The ATK's compiled UGen component releases are available from the <a href="https://github.com/supercollider/sc3-plugins/releases" target="_blank">sc3-plugins releases</a> page.</p>

&nbsp;

<p>Place the downloaded <code>SC3plugins</code> folder in your <code>Extensions</code> folder. On Mac OS X, this resolves to:</p>

<p style="margin-left: 40px"><code>~/Library/Application Support/SuperCollider/Extensions</code></p>

<p>You may need to create the <code>Extensions</code> folder if it does not already exist.</p>  

&nbsp;

<p>On other platforms, you can find where this is by running the following line of code in SuperCollider:</p>

&nbsp;

<pre>
(
// post the directory in which to move the SC3Plugins folder
Platform.userExtensionDir.postln;
)
(
// alternatively, SC can open it for you
// (assuming it already exists! - you may need to create /Extensions)
Platform.userExtensionDir.openOS;
)
</pre>

<h3>Kernels, Matrices & Recordings</h3>

<p>Additionally, the SuperCollider3 version of the ATK has a number of dependencies:<br/><br/></p>

<ul>
  <li>Download and install <a href="/download/kernels">ATK Kernels</a>.</li>
  <li>Download and install <a href="/download/matrices">ATK Matrices</a>.</li>
  <li>Download and install <a href="/download/recordings">ATK Sound File Example Recordings</a>.</li>
</ul>

<p>&nbsp;</p>

<p><strong>NOTE:</strong> The ATK requires SuperCollider3 version 3.5 or later. Download the latest version <a href="http://supercollider.github.io/download" target="_blank">here</a>, or fork the source code at <a href="http://supercollider.github.io/" target="_blank">GitHub</a>.</p>

</div>

&nbsp;

### Source code

You can build ATK for SuperCollider from the [sc3-plugins](https://github.com/supercollider/sc3-plugins) source-code.


### License

<a rel="license" href="http://www.gnu.org/copyleft/gpl.html"><img alt="GNU General Public License" style="border-width:0" src="http://www.gnu.org/graphics/gplv3-88x31.png" /></a><br />The Ambisonic Toolkit for SuperCollider is free software, and is published under the [GPLv3](http://www.gnu.org/copyleft/gpl.html) free software license.

The development of ATK for SuperCollider is supported by <a href="https://dxarts.washington.edu/" target="_blannk">DXARTS &ndash; Center for Digital Arts and Experimental Media</a>.
