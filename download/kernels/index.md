---
layout: page
title: Download Kernels
permalink: /download/kernels/
---

For full featured encoding and decoding, ATK kernels are required.

## Installing kernels for SuperCollider

Install the ATK as above, then download the kernels from here.

Launch SuperCollider3 and run the following code:

ATK Kernel Installation
(
// Create ATK support directory
// Place unzipped kernels in the directory opened  

Atk.createUserSupportDir;
Atk.openUserSupportDir;
)

If the ATK has been correctly installed, the above code will open the ATK's user support directory. Place the downloaded kernels here.

## Installing kernels for Reaper