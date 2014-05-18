---
layout: post
title: "The PRU Speak project"
date: 2014-05-17 22:54:41 +0530
comments: true
categories: [ Beaglebone, opensource, GSoC ]
---

I received some really good news earlier this month! I had been selected for [GSoC 2014][]!


{% img center /images/the-pru-speak-project/GSoC-2014.jpg GSoC-2014 %} 

The project I will be working on the [PRU Speak][] project for [Beagleboard][] this summer :D
The summary of all the projects that have been selected for GSoC-2014 @ Beagleboard is put up at the official [projects page][]

{% img center /images/the-pru-speak-project/BBB-logo.jpg Beaglebone black logo %}

The key motivation behind my project is to make simple the control of the PRU from an userspace process in Linux running on ARM. This is done by developing a custom firmware for the PRU and an API frontend for the user space application to use. A kernel driver forms the bridge between the user spcae library and the PRU firmware, (i.e.) API <--> Driver <--> firmware on PRU.

{% img center /images/the-pru-speak-project/beagleboneblack.png Beaglebone black %}

Here is a small video I wipped up for the organisation that summarizes my project!



<div class="embed-video-container"><iframe src="http://www.youtube.com/embed/8g8e4AgDqNo " height="380" width="680"></iframe></div>




[GSoC 2014]: http://www.google-melange.com/gsoc/homepage/google/gsoc2014
[PRU Speak]: https://github.com/deepakkarki/pruspeak
[Beagleboard]: http://www.beagleboard.org/
[projects page]: http://elinux.org/BeagleBoard/GSoC/2014_Projects

[img-1]: {{root_url}}/images/the-pru-speak-project/GSoC-2014.jpg
