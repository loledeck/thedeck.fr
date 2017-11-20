---
layout: post
title: Visible text in a NSTextContainer backed UITextView
tags: [coding]
---

You cannot easilly get the visible text of a `NSTextContainer` backed `UITextView`. If you look at the `text` or `attributedText` properties, you will get the whole text that you gave to your `NSTextStorage` object.

To get the currently displayed text, I use the following method on my `NSTextView` subclasses:

```objc
- (NSString *)visibleText {

    NSRange currentRange = [self.layoutManager glyphRangeForTextContainer:self.textContainer];

    if (currentRange.location != NSNotFound && currentRange.location + currentRange.length <= self.textStorage.length) {
        // It's safe to use range on str
        NSString *currentString = [self.textStorage.string substringWithRange:currentRange];

        return currentString;
    } else {
        return nil;
    }
}

```
