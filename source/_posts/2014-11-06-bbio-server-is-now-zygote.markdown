---
layout: post
title: "BBIO-Server is now Zygote"
date: 2014-11-06 14:10:36 +0530
comments: true
categories: [AOST, opensource, zygote] 
---

To make the project generic and portable, we are moving the **BBIO-Server** code out the the PyBBIO repository and have created a new project at [zygote][1]

The architecture is as shown in the diagram : 
<img src="https://raw.githubusercontent.com/wiki/kres/zygote/zygote-architecture.png" class="centre" title="Zygote-Architecture"/>

The base block seen in red represents the hardware platform (Raspberry PI, Beaglebone Black, Radaxa board, etc.) on which the application runs on. The platform should have a python based IO library which the zygote server can utilize. There is a generic IO library mapping that happens which maps the board specific python functions to a generic interface which the zygote-server (Flask based RESTful server) uses. This layer also takes a python dictionary which contains the board configurations. The Flask server will use the generic interface to expose a REST api to the external world.

This REST api can be accessed through a mobile or web client, as shown in the diagram. 

[1]: https://github.com/kres/zygote
