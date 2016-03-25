---
layout: post
title:  "Electron data consumption"
date:   2016-03-24 13:20:29 +0100
categories: Rotilio
---

We start to use [Electron](https://www.particle.io/cellular) the new cellular IoT board that works with 3G and 2G cellular module.

The new [Particle.io](https://www.particle.io) product arive in your office or home in a nice plastic box with a microcontroller, SIM card, antenna, 2000mAh battery, USB cable and breadbord for star right away your project.

![Electron](../img/post/electronpack.jpeg)

In this article we want talk about the data consumption.

## Just to be alive

An Electron that is breathing cyan and doing nothing else currently pings every 23 minutes. The ping and the cloud's acknowledgement are each 61 bytes. 

That averages out is to 318 bytes per hour.

This make Electron a low-coast data solution compared to Photon that averages out is to 196 bytes every 15 seconds, or almost 46 kilobytes per hour, just in pings.

The change  to [UDP](https://en.wikipedia.org/wiki/User_Datagram_Protocol) from [TCP](https://en.wikipedia.org/wiki/Transmission_Control_Protocol) produce this increase on performance.

The TCP frame is 20 bytes, plus every message is acknowledged at the TCP level adding another 20 (TCP) + 20 (IP) for the ACK instead the UDP frame is 8 bytes. 


## Every publish and read variable 

When data is sent to or from the device, we have a consumption for a very short Particle.publish of nearly 128 bytes, mostly comprised of infrastructure.

The data infrastructure are the User Datagram Protocol (UDP) 26 bytes, the Datagram Transport Layer Security ([DTLS](https://en.wikipedia.org/wiki/Datagram_Transport_Layer_Security)) 27 bytes and an acknowledgement message ([ACK](https://en.wikipedia.org/wiki/Acknowledgement_(data_networks))) 61 bytes.

## How to limit data consumption

-- Use USB firmware update instead OTA firmware update

-- Publish only if a value is really and significantly changed (send temperature only if it varies more than .5°C)

-- Count the publish per period and limit the publish frequency if possible 

-- Don't poll for variable if is not necessary 

-- Reduce variable and event name length to the minimum

-- Accumulate publish and variables in one time (string concat):

	-- maximum string length for variable value is 622 bytes	
	-- maximum string length for publish data is 255 bytes	
-- Use System.sleep() to reduce data exchange (and Pfv) [https://docs.particle.io/reference/firmware/electron/#sleep-sleep-](https://docs.particle.io/reference/firmware/electron/#sleep-sleep-)

-- If possible write firmware with this two guide lines:

	--	work even if in offline mode (ex: if data limit reached, Electron goes offline)
	
	-- work with local algorithm if you can, to avoid dialog with the cloud

