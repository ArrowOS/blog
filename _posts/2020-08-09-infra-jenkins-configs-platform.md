---
layout: post
title: "ArrowOS configs platform guide"
description: "A basic guide on how to use configs platform for our internal contributors."
thumb_image: "https://raw.githubusercontent.com/ArrowOS/arrow_logos/master/ArrowLogo-sky-transparent.png"
priority: 1002
tags: [arrowos, android, news, infra, team, configs]
---

Published on: Aug 09, 2020 by Kuber Sharma, Ganesh Varma<br>

<style type="text/css" media="Screen">
 .Dropcap {
  color: #42f5aa;
  float: left;
  font-size: 69px;
  line-height: 30px;
  padding-top: 4px;
  padding-right: 8px;
  padding-left: 3px;
}
</style>

<span class="Dropcap">H</span>ello, contributors (and future contributors?), we will go through our configs platform on today's blog post/article or whatever you calll it.

As, we said in our [previous post](https://blog.arrowos.net/posts/infra-team-configs-briefing), that configs "acts as an interactive bridge between jenkins and the pipeline in handling independent device parameters via a neat web interface without the hassle of going through CLI". It has surely made our lives easy with overall project management.

#### Getting access to configs
<center><img src="https://raw.githubusercontent.com/ArrowOS/blog/arrow/_assets/images/configs-login.PNG">configs login page</center>

The username (will most likely be a contributors github or telegram username) and initial login passwoerd will be assigned by the CORE team when a new contributor joins the team.

#### Just logged in, what's next?

This is where the fun begins!

<center><img src="https://raw.githubusercontent.com/ArrowOS/blog/arrow/_assets/images/dashboard.PNG">Main dashboard</center>

This is where the device(s) which a contributor will manage/maintain shows up, as in the above screenshot you can see that it shows all supported ArrowOS devices are shown for me that is just because as a CORE member I have Admin rights.

Now, lets move on to how it looks like when we select a device.

<center><img src="https://raw.githubusercontent.com/ArrowOS/blog/arrow/_assets/images/devices-d.PNG"></center>

This is how it looks like when you select a device, as you can see there are bunch of features and options inside. I will explain what they do below:

<b>Weeklies</b> toggle: This indicates whether you want your device to be built for the next official weekly or you want to skip your device from next weekly. A maintainer is only allowed skip next 3 weeklies only before the device is removed from the official support.

<b>"Path of repos to delete!" AND "Url's of repos to clone/sync!"</b>: This is generally for when you want to test something from a different branch or a different repository, for example I forked android_device_xiaomi_beryllium and made some changes which i want to test before pushing to ArrowOS-Devices org.
I will put device/xiaomi/beryllium into "Path of repos to delete!" textfield and My forked repository git link with path i.e device/xiaomi/beryllium with the branch were i made changes example: staging-changes

<b>Repopick topics!</b>: To pick a topic from our gerrit/codereview in your device's next build

<b>Repopick change numbers!</b>: To pick commits based on their change numbers in your device's next build.

Now, lets scroll below..

<center><img src="https://raw.githubusercontent.com/ArrowOS/blog/arrow/_assets/images/devices-d2.PNG"></center>

<b>XDA thread link:</b> This is where you link your XDA thread of your device, leave it empty if you have not posted in XDA forum yet. You can also post in other forums and ask the CORE team if you can link that instead. We may surely allow you.

<b>Changelog:</b> This is where you define your device specific changelogs, this will be shown in our [downloads page](https://arrowos.net/download.php)

<b>Push button</b>: really? haha. This will save your changes but won't initiate a build compilation.

<center><img src="https://raw.githubusercontent.com/ArrowOS/blog/arrow/_assets/images/devices-d3.PNG"></center>
These do what they say they do. Build builds, abort aborts etc nothing fancy.

<b>NOTE:</b> <br>
* Build button will save your changes and initiate a build compilation.
* When WEEKLY builds are running, you won't be able to initiate a test build.
* Before OFFICIAL WEEKLY starts, you should clear your test config changes and set device changelogs as you see fit.
* You can use configs to make test builds anytime, as many times as you like.
* When you toggle "Boot Image" toggle, it will only compile boot.img

The builds compiled by a contributor goes to our [experimental builds org in sourceforge](https://sourceforge.net/projects/arrowos-experiments/)

#### Stay home, Stay safe!

#### Want to contribute? and one day earn a spot in the CORE team? <br>

[Checkout this post](https://blog.arrowos.net/posts/apply-for-maintainership)

###### Write to us about your thoughts at <arrowos.contact@gmail.com> and in the comments section below. <br>