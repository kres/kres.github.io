---
layout: post
title: "PRU Speak - Project updates"
date: 2014-06-02 00:05:57 +0530
comments: true
categories: [ Beaglebone, opensource, GSoC, PRU-Speak ]
---

It's been over two weeks since I started on my [GSoC project][], and what a journey it's been! Reading thousands of lines of kernel code, prototyping my own drivers and involved discussions with the community members :D 

Here is the update : 

* Tried out character drivers
* Developed my own sysfs driver with support for both binary and device files.
* Hacked on my mentors driver.
* Got upcalls and down calls working. 
* Developed some C + Assembly based firmware for the PRU
* Shared memory implementation between the kernel and PRU.
* currently working on exporting the shared memory to userspace. 

[GSoC Project]: https://github.com/deepakkarki/pruspeak
