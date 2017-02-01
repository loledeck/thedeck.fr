---
layout: post
title: Finding the UTI of a PEM certificate on iOS
tags: [coding, iOS]
---

UTI stands for "Uniform Type Identifiers". 

It's like the definition of a file type tying together files extensions, mime types and higher level UTIs.
In iOS (and macOS also I guess) you have to provide UTI(s) to initialize the ```UIDocumentMenuViewController``` class, also known as the "iOS Document Picker". This list will tell the system which type of files your Document Picker will be allowed to open.

This is all good and well unless you don't know which UTI to use for the file type your looking for. 

I was trying to import pem certificates into one of my apps and didn't know which UTI to use for this task. Fear not, fair developer, Apple said ! Head to our official list of [System Declared Uniform Type Identifiers](https://developer.apple.com/library/content//documentation/Miscellaneous/Reference/UTIRef/Articles/System-DeclaredUniformTypeIdentifiers.html).

Of course, no declared UTI covered my use case. Or so I thought ...

Having wrestled with this issue for the better part of the day I have at last found this *very* useful site: [UTI type browser](http://uti.schwa.io). 

It's the UTI list that Apple should have provided. There are much more types available than the one listed in the official Apple documentation. Including the one I needed:

```
public.x509-certificate
```
