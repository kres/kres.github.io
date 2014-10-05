---
layout: post
title: "BBIO-Server"
date: 2014-09-25 21:42:15 +0530
comments: true
categories: [AOST, opensource, PyBBIO] 
---

As we had talked about in our last post, We'll be working on BBIO-Server as our AOST (Architecture of Open Source Technologies) project. This will be an extension to Alexander Hiam's work, [PyBBIO][1]!

Currently the [BBIO-Server][2] is implemented as a library in the PyBBIO project. It enables the users to build a web page via a python API. Lambda functions help enable the RPC mechanisim to link user action on the web page to hardware actions on the Beaglebone Black. [Here][3] is the overview of how to use the API. 

	NOTE : These links will change overtime, the current library may soon be depreciated. 

Our proposal is to replace the current implementation as it has a few shortcomings. One of the problem being that there is no clean way to access hardware end points from the client side. The page has to be built using the BBIO-Server API; there is no other generic way to access the IO pins on the board. We plan to tackle this problem by developing a RESTful API to access hardware as follows : 
```
GET /bone/gpio/2?pin=3
```
gets the status of pin 3 of the 2nd GPIO module (the BBB has 4 GPIO modules). To set the pin status, 
```
POST /bone/gpio/2 {pin : 3, status : "HIGH"}
```
to setup a sensor/actuator on a paritcular port, we will be using the PUT request
```
PUT /bone/pwm/1 {pin : 2, type : "SERVO"}
```

Also the current implementation is a custom built HTTP server using the python HTTP API. It makes more sense to use a existing lite server side framework such as [Flask][4].

Another limitation of the current implementation is that you can't directly access the hardware from the client side, i.e. you have to build the page using the python API only, which is not very nice for most developers. This calls for a neat javascript based API which will give developers a neat way to control the BBB via a web interface. Such as
```
digitalWrite(1, HIGH);
servo.setAngle(120);
```
Additionally we propose to create an API for data streaming via web-sockets/web-rtc. This will be useful for sensor data graphing and video camera display.

Finally developers would like to have ready to use UI components at their hands, and for this purpose we will be integrating BBIO-Server with [Freeboard][5] and also adding our custom UI components! 

Note : A similar project is [Web-IO-Pi][6] which enables web page based hardware control on the Raspberry PI.

[1]: https://github.com/alexanderhiam/PyBBIO
[2]: https://github.com/alexanderhiam/PyBBIO/blob/master/libraries/BBIOServer
[3]: https://github.com/alexanderhiam/PyBBIO/wiki/BBIOServer
[4]: http://flask.pocoo.org/
[5]: https://freeboard.io/
[6]: https://code.google.com/p/webiopi/
