---
layout: page
title: Download ATK for SuperCollider 3
permalink: /download/supercollider/
---

&nbsp;

<div class="alert alert-info">

<h2>Distributed via the <a href="http://sc3-plugins.sourceforge.net/" target="_blank">sc3-plugins</a> project.</h2>

<p>On Mac OS X, the sc3-plugins download can be placed into the <code>Platform.userExtensionDir</code> folder. You can run the following code to open the Extensions directory:</p>

<p>&nbsp;</p>

<pre>
sc3-plugins Installation
(
// Place sc3-plugins Extensions in the directory opened  

Platform.userExtensionDir.openOS
)
</pre>

<p>&nbsp;</p>

<p>You may also wish to review the documentation on [Using Extensions](http://doc.sccode.org/Guides/UsingExtensions.html).

If building from source for OS X, Windows or Linux, follow the sc3-plugins build and install directions.</p>

<p>Additionally, the SuperCollider3 version of the ATK has a number of dependencies. Please install the following:<br/><br/></p>

<ul>
  <li>Install the <a href="http://quarks.svn.sourceforge.net/viewvc/quarks/MathLib/" target="_blank">MathLib</a> Quark via the instructions found <a href="http://quarks.sourceforge.net/" target="_blank">here</a>.</li>
  <li>Download and install <a href="/download/kernels">ATK Kernels</a>.</li>
  <li>Download and install <a href="/download/recordings">ATK Sound File Example Recordings</a>.</li>
</ul>

<p>&nbsp;</p>

<p><strong>NOTE:</strong> The ATK requires SuperCollider3 version 3.5 or later. Download the latest version <a href="http://supercollider.github.io/download" target="_blank">here</a>, or fork the source code at <a href="http://supercollider.github.io/" target="_blank">GitHub</a>.</p>

</div>

&nbsp;

### Source code

You can build ATK for SuperCollider from the [sc3-plugins](https://sourceforge.net/projects/sc3-plugins/) source-code.

&nbsp;

### License

Ambisonic Toolkit for SuperCollider is free software, and is published under the <a href="http://www.gnu.org/copyleft/gpl.html" target="_blank">GPLv3</a> free software license.
