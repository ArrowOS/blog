---

layout: post
title: "How to report a bug!"
description: "Reporting bugs in android OS or our Infra"
thumb_image: "https://raw.githubusercontent.com/ArrowOS/arrow_logos/master/ArrowLogo-sky-transparent.png"
priority: 1004
tags: [arrowos, android, news, bugs]
---

Published on: Nov 28, 2020 by Kuber Sharma<br>

<style type="text/css" media="Screen">
 . Dropcap {
  color: #42f5aa; 
  float: left; 
  font-size: 69px; 
  line-height: 30px; 
  padding-top: 4px; 
  padding-right: 8px; 
  padding-left: 3px; 
}
</style>

<span class="Dropcap">I</span>n this blog post, we will talk about on how to report bugs in our fork of AOSP platform and infrastructure which includes website, downloads server, statistics webpage and more.

#### Things you CANNOT report:

* Bugs which are present in unofficial builds or anything not downloaded from our official downloads server
* Asking about device support, unlocking bootloader, getting TWRP installed
* Bugs on a device which has root privelleges from SuperSU, Magisk etc
* Feature requests in the OS
* Supporting a new device

#### Reporting a bug

We use Gitlab Issues as our bug tracker, you can report [infra](https://gitlab.com/arrowos-support/issues/infrastructure/-/issues/new) or [ArrowOS android platform](https://gitlab.com/arrowos-support/issues/android/-/issues/new) bugs there.

#### How to report a bug?

Check if someone has already reported that bug before you create a new issue, incase you find there is already a bug report for it you can comment there with "+1" OR "I am also facing this" etc BE CREATIVE.

Please, report bugs in the same manner as mentioned below for the following:

* ArrowOS android platform
Example:
"Hey, I faced a bug in arrow-11.0 on my Elgoog Pixel XL. Camera is broken it doesn't work. I uploaded the logcat here wwwdotsomethingdotcom/camera-logs.txt"

* ArrowOS Infra
Example:
"Hey, on ArrowOS website, official supported device list just vanished, I cannot download anything"

