---
layout: post
title: 2 Elements that Sums 0
categories: [Objective-C]
tags: [Objective-C]
fullview: true
comments: true
---

*Question*: **Given an array of integers [-1,1,2,4,3] return true if there are 2 elements that sums 0**.  

  Use NSMutableDictionary, the key is (0-number), the value is number, so that we can lookup/insert efficiently. 

```objc
-(BOOL) sumsToZero:(NSArray *)array;
{
   NSMutableDictionary *dictionary = [NSMutableDictionary dictionary];
   for (NSNumber *number in array) {
    if ([dictionary objectForKey:number]) {
        return true;
     } else {
        NSNumber *numNeeded = [NSNumber numberWithInt:0 - [number integerValue]];
        [dictionary setObject:number forKey:numNeeded];
     }
   }
   return false;
}
```