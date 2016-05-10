---
layout: page
title: Download ATK for SuperCollider 3
permalink: /download/supercollider/
---

&nbsp;

<div class="alert alert-info">

<h2>Distributed via the <a href="https://github.com/supercollider/sc3-plugins" target="_blank">sc3-plugins</a> project.</h2>

<p>Compiled releases are available from the  <a href="https://github.com/supercollider/sc3-plugins/releases" target="_blank">sc3-plugins releases</a> page.</p>

&nbsp;

<p>Place the downloaded <code>SC3plugins</code> folder in your <code>Extensions</code> folder. On Mac OS X, this resolves to:</p>

<p><code>~/Library/Application Support/SuperCollider/Extensions</code>.</p>

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

<p>Additionally, the SuperCollider3 version of the ATK has a number of dependencies. Please install the following:<br/><br/></p>

<ul>
  <li>Install the <strong>MathLib</strong> Quark most simply by running <code>Quarks.gui</code> in the SuperCollider IDE. Further install options and informations on Quarks can be found in SuperCollider's Help system, see <a href="http://doc.sccode.org/Guides/UsingQuarks.html" target="_blank">Using Quarks</a>, and also at the <a href="https://github.com/supercollider-quarks/quarks" target="_blank">supercollider-quarks GitHub page</a></li>
  <li>Download and install <a href="/download/kernels">ATK Kernels</a>.</li>
  <li>Download and install <a href="/download/recordings">ATK Sound File Example Recordings</a>.</li>
</ul>

<p>&nbsp;</p>

<p><strong>NOTE:</strong> The ATK requires SuperCollider3 version 3.5 or later. Download the latest version <a href="http://supercollider.github.io/download" target="_blank">here</a>, or fork the source code at <a href="http://supercollider.github.io/" target="_blank">GitHub</a>.</p>

</div>

&nbsp;

### Source code

You can build ATK for SuperCollider from the [sc3-plugins](https://github.com/supercollider/sc3-plugins) source-code.

&nbsp;

### License

Ambisonic Toolkit for SuperCollider is free software, and is published under the <a href="http://www.gnu.org/copyleft/gpl.html" target="_blank">GPLv3</a> free software license.
