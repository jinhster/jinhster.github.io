---
layout: post
title:  "Loading Testing with fiddler and Stresstumulus"
date:   2015-02-27
categories: ruby
---

Fiddler is a web debugger that captures all the traffic (in and out ) you processes. Most people mainly uses on browsers, so they can capture information sending out and getting in through browsers (IE, firefox, chrome etc.). Key features of fiddler includes: web debugging, performance testing, traffic recording, web session manipulation, security testing and with plugins like stresstimulus you can do load testing.


stresstimulus is a web loading testing tool that works with or without fiddler (its better to have it with fiddler so you enjoy the benefit what fiddles has to offer).

Lets first download [fiddlers](http://www.telerik.com/fiddler) and [stresstimulus](http://www.stresstimulus.com/)

After that open fiddler and try going to a site.
Fiddler will log all the traffic that you are currently using.
Select all and create a test case with stresstimulus commands.

![Imgur](http://i.imgur.com/wpfuw3Z.png =900x)

Press next

![Imgur](http://i.imgur.com/3toC3Z9.png =900x)

Filter the external site (Some site will use external link like google analytics).

![Imgur](http://i.imgur.com/6cPwWnN.png =900x)

Next

![Imgur](http://i.imgur.com/ZDuBFf8.png =900x)

Choose amount of virtual users you want to use for the load testing.

![Imgur](http://i.imgur.com/InqsBNj.png =900x)

You can even do a step load (Setting timer on virtual users, like when the users will increase over time).

![Imgur](http://i.imgur.com/jGf6oP9.png =900x)

How many number of iterations you want the users to do.

![Imgur](http://i.imgur.com/XSi30IK.png =900x)

Press run test

![Imgur](http://i.imgur.com/HE7VRhD.png =900x)

You can observe the graph for load over time and see how it perform.

![Imgur](http://i.imgur.com/SsORr5O.png =900x)

After you are done stresstumulus will generate a report for you.

![Imgur](http://i.imgur.com/pAvQRKQ.png =900x)


Since we are on fiddler there's a trick in fiddler, works like the network tab in developer's tool in chrome and other browsers, but better. Why? I will show you.

![Imgur](http://i.imgur.com/9U4li1e.png =900x)

You can actually change the performance of the traffic (You can set it to simulate modem speeds (Highest is 56KB/s if you are wondering)).

![Imgur](http://i.imgur.com/yjGNhfb.png =900x)

See how slow it is now?

Thanks.
