---
layout: post
title: "BBIO-Server Development - 2"
date: 2014-10-22 21:54:30 +0530
comments: true
categories:  [AOST, BBIO-Server, opensource]
---

Currently we have developed the basic RESTful API for the BBIO-Server. The functionality currently supported includes : GPIO, PWM, analog in, Servo and custom modules.

Sample interfaces 
```

GPIO handler : 
	GET	/gpio/1/16?task=write&state=HIGH	:: sets pin GPIO1_16 high
	GET	/gpio/1/16?task=config&mode=INPUT	:: sets pin to input mode
	GET 	/gpio/1/16?task=read				:: reads pin, returns status

PWM handler :
	pwm to work with default configuration.
	i.e. freq = 10KHz and resolution = 8 bit

	pin to pwm mapping :-
	P8.13 - PWM2B
	P8.19 - PWM2A
	P9.14 - PWM1A
	P9.16 - PWM1B

	GET /pwm/1A?value=10
	
Analog In : 
	function to handle ADC read requests. 
	Input can be from 0 - 1.8V, o/p of 12 bit resolution

	P9.33 - AIN4
	P9.35 - AIN6
	P9.36 - AIN5
	P9.37 - AIN2
	P9.38 - AIN3
	P9.39 - AIN0

	GET /adc/AIN0 => returns the analog input at channel 0
	
Servo controller :
	each servo is attached to a PWM module

	GET /servo/PWM1A?config=enable	=> enables this module
	GET /servo/PWM1A?angle=50 	=> moves servo to 50 deg
	GET /servo/PWM1A?config=disable	=> disables this module
```

Here is the code that has been currently written :
<script src="https://gist.github.com/deepakkarki/5e767d25dd2fae4a07b8.js"></script>


