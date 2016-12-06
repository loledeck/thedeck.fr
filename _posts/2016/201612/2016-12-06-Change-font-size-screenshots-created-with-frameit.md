---
layout: post
title: Change font size in screenshots created with Frameit
tags: [coding]
---

[Frameit](https://github.com/fastlane/fastlane/tree/master/frameit) is a very nice utility to create nice looking App Store screenshots. It will take your images, add a device frame around them and optionaly a title of your choosing in multiple language. In short, it's a godsend.

But unfortunatly, as any tool, it has a few shortcomings. One of them (for my use case at least) is that there's no way to choose the size of the font you're using for your titles.

For example, look at this screenshot for my app [Librairie - Ebook Cloud Reader](https://itunes.apple.com/us/app/librairie-ebook-cloud-reader/id742022507?mt=8&at=1010lrXT):

![Bad screenshot](/assets/images/201612/screenshot_bad.png)

It's not bad per se but it could be much better with a bigger font to add some punch. The corresponding json is:

```json
        {
            "filter": "collection",
            "title": {
                "color": "#bc1626"
                ,"text": "Automatically sync and read all your ebooks stored in the cloud"
            }
        }
```        

The trick is to make Frameit think that the text will take more space and as a consequence use bigger font to fill that space. For this, you can use a new line character in your description. The *Framefile.json* becomes:

```json
        {
            "filter": "collection",
            "title": {
                "color": "#bc1626"
                ,"text": "Automatically sync and read all\nyour ebooks stored in the cloud"
            }
        }
```

And the rendered screenshot:

![Good screenshot](/assets/images/201612/screenshot_good.png)

Et voilà !
