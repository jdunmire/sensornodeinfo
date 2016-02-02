---
layout: post
title:  "Sensor Node power considerations"
author: Jerry
#date: YYYY-MM-DD  # last modified if different than the filename/modification time
permalink: /blog/YYYY/MM/DD/unique-name
#commentIssueId: <issue number>  # optional, no comments if not defined
categories:
- blog
- <one or more categories, one per line>
img: 640x480_image.jpg|png
thumb: 70x53_image.jpg|png or 70x70_image.jpg|png

---
Regulators - boost, boost-buck, charging circuits
Need way to measure the battery voltage
Regulator draws power. Disabling is an option, but need to have some
other way to get power.

Adds cost, complexity, and increases power consumption.

Battery
  - Alkaline - voltage is not stable and a boost regulator is required
      to make full use of the capacity.
  - Li/LiPoly - Need buck regulator. Issues with charging and safety.
  - LiFePO4 - Almost the full capacity can be used without a regulator.
      Lower power density. Needs careful charging, but not a quite as
      critical as Li/LiPoly.

