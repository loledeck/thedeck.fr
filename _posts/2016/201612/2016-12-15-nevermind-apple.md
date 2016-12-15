---
layout: post
title: Nervermind Apple
tags: [apple]
---

I just wanted to take advantage of one of the coolest looking feature of watchOS 3 : the auto unlocking of your mac.

Well, the first step is to enable *2 factors authentification* for your iCloud account. My account was already on the *2 steps authorization* scheme so that should be a piece of cake, right ?

Wrong, so f***ing wrong.

You first have to downgrade your account to go back to the classic protection by security questions. By doing so, macOS asked me to create a new user because I used my iCloud account to log into my mac and for some reason that was not possible anymore. 

Okay ... I guess ? 

At this point I had no real choice anyway so let's go ahead : create a new password and that's it, you have your new user identical to the previous one (or so it seems, keep reading ...).

Then upgrade your iCloud account to *2 factors auth* : Oh boy ! There's nothing that makes me like doing my taxes more than a good old fashioned self imposed Apple nightmare ...

When you activate *2 factors auth* you have to validate each device you use (iPhones, iPads, Macs) with a second factor. This second factor being (it's the only option) a prompt that appears on one of your trusted devices. The problem being that each of my devices were then asking for a validation and that none of them was showing me the said prompt.

So what can you do ? After several reboots, logout / login again cycles ... you give up. That's for sure what I did. I reverted my iCloud account back to security by *security questions* (because of course the *2 steps verification* scheme is not available anymore once you have *upgraded* to *2 factors auth*).

And now, the kicker: remember my macOS account that *seemed* OK. Well it was not. The session password was now de-synchronized from the FileVault password that I have to provide at each reboot to decrypt my hard-drive. So each time I rebooted I had to enter the FileVault rescue key.

Had I not set a FileVault rescue key (which would have been stupid sure, but what if you've lost it ?) trying to unlock my Apple Mac with my Apple Watch through my Apple iCloud account would have nixed all my data.

Let that sink in.

So thanks Apple and next time would it be possible to ... No, you know what, nevermind. It's on me. 

Next time I won't even try.