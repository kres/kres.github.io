---
layout: post
title: "First look at PRU Speak API"
date: 2014-06-14 20:13:42 +0530
comments: true
categories: [ Beaglebone, opensource, GSoC, PRU-Speak ]
---

I managed to get a basic ARM userspace to PRU interaction up and running and even wrote a python API to take care of the interactions.
Here is how the API looks like!

```python
import pru_speak
 
botspeak_code   = \
'''     SET DIO[0] , 1
        WAIT 1
        SET DIO[0], 0
        WAIT 1
        GOTO 0'''
 
pru_speak.load(botspeak_code)
pru_speak.execute()
```
