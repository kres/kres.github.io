---
layout: post
title: "AOST Project"
date: 2014-09-12 20:39:10 +0530
comments: true
categories: [AOST, Open Source, project, PyBBIO] 
---

This semester, I have chosen AOST (Architecture of Open Source Technologies) as my group C elective. As a part of the course we are required to contribute to an open source project. 
I'm pleased to announce that me and my teammate Aishwarya, will be contributing to PyBBIO <link>.

------
PyBBIO aims to provide a arduino like interface for controlling the IO modules on the BeagleBone Black. Currently there is support for GPIO, UART, SPI, I2C, Camera and host of other sensors. We plan to contribute the BBIO-Server library through the course of the semester. BBIO-Server will be an extremely versatile tool for developing IoT prototypes. It will have all the necessary components ranging from UI to a RESTful backend service that enables interacting with the BeagleBone's IO (using PyBBIO) across an HTTP connection. 

Specifics of the project include : 

*	 Creating a RESTful API to access hardware interfaces via PyBBIO (can be thought of as making RPCs).
	
	For example to initialize a sensor ```PUT /bbio/spi/adt7310  "{'bus':'SPI1','cs':'GPIO1_16'}"``` or to get a value ```GET /bbio/spi/adt7310/temp "{'units':'C'}"```
*	 A javascript frontend API (ajax based) for making calls to the server (wrapper for the RESTful HTTP service)
*	 Interface for full duplex data streaming using Socket.io
*	 Standard set of UI components (integrated with Freeboard) to get the developer started with zero effort.

