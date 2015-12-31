---
layout: post
title: "Dead Battery"
date: 2015-11-24
author: Jerry
permalink: /blog/2015/11/24/deadbattery
categories:
- blog
- T&L Node
- T&L Node Firmware
img: TLnode_144x108.png
thumb: TLnode_70x53.png
#commentIssueId:3

---
One of my T&L Nodes drained its battery in less than 24 hours!

I've been trying out the new LiFePO4 batteries on this unit. The
performance has been far less than I expected. After only a week or so
on a the last charge I've been trying different batteries to narrow down
the problem. So on Sunday I put in a new, freshly charged battery and by
Monday evening the unit was dead. That doesn't seem like a battery
problem.

The next thing I noticed was that is that the communications LED was
flashing every few seconds, rather than every 5 minutes. Looks like the
node is not going into deep sleep. That would explain the rapid battery
drain, but why?

Install firmware with debugging enabled. Good plan, but the flash
failed! But I haven't written to flash enough to cause a flash failure.
A bit of time on Google and I found some others that had flash failures
which appear to have been solved in recent version of esptool.py.

Good news, a new verison of the esptool.py solves the flash failure
problem. Bad news, the debug messages show that the node is rebooting
when it tries to establish a WIFI connection.

The WIFI connection was working, and other WIFI devices are still
working, but use a scanner just to check. The AP is now using channel 11
and I think it was on channel 6 in the past. The AP was reset on Monday,
maybe the node is having a problem with channel 11?

Why aren't the other nodes showing a similar problem?

More to follow.
