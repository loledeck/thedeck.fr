---
layout: post
title: App Action Extension icon in XCode 8
tags: [coding, xcode]
---

Aaaarrgghhhh !!!

<br>
<br>
That's generaly what I say when XCode decides to mess with me. Today I was writing an new action extension for my [Librairie app](http://librairie.cubesoft.fr) (note that it's the first one I write with XCode 8).

Everything goes fine until I decide to give an icon to this sad little white square used to launch my extension. Normaly I'd go to your target settings "General" tab and choose the asset catalog containing your icon.

![General tab](/assets/images/2016-09-29-app-extention-icon-xcode-8/general-tab.png)

But no, no dice ...

Some smart product manager at Apple decided that it would be fun to see how long it would take me to do my job if they just removed the UI that they previously designed just for this purpose. The answer to this question is precisely ... quite some time.

Turns out, you have to go to the build settings of your target and find the "Asset Catalog App Icon Set Name". There, you enter the name you have given to your app icon folder (the folder with all the different icon sizes *inside* your asset catalog). 

![Build settings](/assets/images/2016-09-29-app-extention-icon-xcode-8/build-settings.png)

Good job Apple ...