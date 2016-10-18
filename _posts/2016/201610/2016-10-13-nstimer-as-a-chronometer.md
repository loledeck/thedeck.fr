---
layout: post
title: NSTimer as a chronometer
tags: [coding]
---

NB: This post is mainly a reminder for myself.
How to create a chronometer in Objective C ? I'm glad you asked:

First, create your NSTimer

```objc
NSTimer *chronometer = [NSTimer scheduledTimerWithTimeInterval:1.0
    target:self
    selector:@selector(addToChronometer)
    userInfo:nil
    repeats:YES
];
```

And store the current time in an instance variable

```objc
NSDate *startTime = [[NSDate alloc] init];
```

The timer will call a function aproximatively every second (*the chronometer will not provide an exact measure of time. It will be used to show time passing in the format 00:00:00*).

```objc
-(void)addToChronometer {	
    NSTimeInterval interval = -1 * [startTime timeIntervalSinceNow];

    NSInteger ti = (NSInteger)interval;
    NSInteger seconds = ti % 60;
    NSInteger minutes = (ti / 60) % 60;
    NSInteger hours = (ti / 3600);

    self.chronoLabel.text = [NSString stringWithFormat:@"%02ld:%02ld:%02ld", (long)hours, (long)minutes, (long)seconds];
}
```

Et voilà !





