---
layout: post
title: Constant freezes with macOS Sierra
tags: [macOS]
---

Since upgrading to Sierra last week, my 5K iMac late 2015 has been quite flaky. More precisely, it has experienced regular freezes that required hard reboots of the machine. When I say regular, I mean 5 or 6 times a day. 

During those freezes, the mouse and keyboard would become unresponsive and the screen saver would never kick in. At the same time, the audio would continue to play and the icons in the menu bar would still be updated.

After trolling the internet and Apple forums for a while, I think I found the culprit: Logitech Control Center.

This is a small utility that let's you fine tune your Logitech mouse and keyboard but requires a kernel extension for doing its magic. Since I disabled it my iMac has not been frozen once (fingers crossed ...). I have lost the butter smooth scrolling of my mouse wheel but that's much better than rebooting all day long. 