---
layout: post
title: "BBIO-Server Development - 1"
date: 2014-10-04 15:48:35 +0530
comments: true
categories: [AOST, BBIO-Server, opensource]
---
As we work on BBIO-Server, we will keep the community updated through this blog. The series of posts will discuss the various steps and design decisions taken by us while developing this library.
In this post we will explain how we setup the environment to get started and start using the PyBBIO API.

##Environment Setup
1. Fork Alexander Hiam's [upstream repository][1] to our [master][2]. The master is where we will be adding our library, which is to be upstreamed once complete.
2. Install the dependencies for PyBBIO as given [here][3] in the official wiki.
3. Clone our master repository from github, create a BBIO-Server-dev branch.
4. Install the code from source, by running setup.py, viz present in the root directory of the project.
5. Install Flask : ```pip install Flask```

This is how we setup the environment to get started.

##Using PyBBIO
Deepak has written a nice tutorial on using the PyBBIO API [here][4].

##Official development branch
The official development tree is [here][5]. This is where we will be commiting our code.

[1]: https://github.com/alexanderhiam/PyBBIO
[2]: https://github.com/kres/PyBBIO/
[3]: https://github.com/alexanderhiam/PyBBIO/wiki/Installing-PyBBIO
[4]: https://github.com/alexanderhiam/PyBBIO/wiki/Using-PyBBIO
[5]: https://github.com/kres/PyBBIO/tree/bbio-server-dev
