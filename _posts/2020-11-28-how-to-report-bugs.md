---

layout: post
title: "HOW-TO report a bug"
description: "Reporting a bug in our ArrowOS android platform or in our Infra"
thumb_image: "https://raw.githubusercontent.com/ArrowOS/arrow_logos/master/logcatorgtfo.jpg"
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

<span class="Dropcap">I</span>n this blog post, we will talk about on how to report bugs in our fork of AOSP platform and infrastructure for it which includes website, downloads server, statistics webpage etc.

<center><img src="https://raw.githubusercontent.com/ArrowOS/arrow_logos/master/logcatorgtfo.jpg"></center>

#### WHAT NOT to report.

* Bugs which are present in unofficial builds or anything that is not downloaded from our official download server,
* Asking about device support, unlocking bootloader, getting TWRP installed and similar stuff,
* Bugs on a device which has root privelleges from SuperSU, Magisk, Magisk Modules etc,
* Isues which suggest feature requests,
* Issues which suggest supporting a new device which we do not own,
* Bugs which arise after replacing default apps,
* Bugs which occur in third party apps,
* Bugs in devices we do not support anymore
* Bugs in ArrowOS experimental builds

#### WHERE to report.

We use Gitlab Issues as our bug tracker, you can report issues/bugs related to [infra](https://gitlab.com/arrowos-support/issues/infrastructure/-/issues/new) or [ArrowOS android platform](https://gitlab.com/arrowos-support/issues/android/-/issues/new) bugs there.

#### HOW to report.

Check if someone has already reported that bug before you create a new issue, incase you find there is already a bug report for it you can comment there with "+1" OR "I am also facing this" etc BE CREATIVE.

Please, report bugs in the similar manner as mentioned below:

* **ArrowOS android platform**
Example:
    * "I am facing a bug in arrow-11.0 community VANILLA edition on my Elgoog Pixel XL. Camera is not working since last update. I uploaded the logcat here www.something.com/camera-logs.txt"
    * "WiFi is not working on my OnePlus One, I use OFFICIAL arrow-11.0 GAPPS build. I have captured a logcat while trying to open WiFi and have upload it to www.somethingd.com/opo-cyberwifi-10-12-2077.log"

        * **Tip:**
            * You can upload logs as an attachment in gitlab issues or upload to websites like hastebin.com etc
                * Here are some articles to help you with capturing logcats in android:
                            1. [https://developer.android.com/studio/command-line/logcat](https://developer.android.com/studio/command-line/logcat)
                            2. [https://www.xda-developers.com/how-to-take-logs-in-android/](https://www.xda-developers.com/how-to-take-logs-in-android/)
            * You MUST provide proper steps to reproduce that bug, glitch or whatever issue you are facing, please dont report your OCD's as bugs
            * Always mention things like:
                * **ArrowOS Version:** arrow-10.0; arrow-11.0; arrow-12.0 etc
                * **ArrowOS Build Type:** OFFICIAL; COMMUNITY; UNOFFICIAL
                * **ArrowOS Build Variant:** VANILLA; GAPPS

* **ArrowOS Infra**
Example:
    * "Official supported device list just vanished on ArrowOS website, I cannot download anything"
    * "ArrowOS gerrit is not opening since an hour, I want to push some of my changes to it"

***
Please properly mention all the details you can gather, capture logcats for android bug reports after reproducing it. If you do not mention the details or if logcats are not provided such reports will be DIRECTLY ignored. Make sure all requirements are correctly fulfilled, incomplete or one sentence reporting of bugs will be ignored. Once you report the bug, please allow some time for maintainers/deveopers to look at it, dont be imaptient and expect the bugs fixed in next update. Critical bugs will be fixed on top prioriity compared to other so please be PATIENT. Last but not the least, please DO NOT SPAM the telegram chat with bugs and feature requests.
