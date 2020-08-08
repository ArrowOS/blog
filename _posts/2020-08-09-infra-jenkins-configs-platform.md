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

<span class="Dropcap">H</span>ello, contributors (and future contributors?), we will go through our configs platform on today's blog post/article or whatever you call it.

As, we said in our [previous post](https://blog.arrowos.net/posts/infra-team-configs-briefing), that configs "Acts as an interactive bridge between jenkins and the pipeline in handling independent device parameters via a neat web interface without the hassle of going through CLI". It has surely made our lives easy with overall project management.

#### Getting access to configs
<center><img src="https://raw.githubusercontent.com/ArrowOS/blog/arrow/_assets/images/configs-login.PNG">configs login page</center>

The username (will most likely be a contributors github or telegram username) and initial login password will be assigned by the CORE team when a new contributor joins the team.

#### Just logged in, what's next?

This is where the fun begins!

<center><img src="https://raw.githubusercontent.com/ArrowOS/blog/arrow/_assets/images/dashboard.PNG">Main dashboard</center>

This is the place where the device(s) assigned to a contributor to manage/maintain show up, as in the above screenshot you can see as a CORE member with admin privileges it displays all the official ArrowOS devices. For a contributor it'll be limited to on only showing the device he/she maintains.

To the left in the Navbar from the profile section, the user will be able to manage their profile related settings (username/password). The maintainers section is ADMIN access only, for managing contributors settings and activity.

Now, lets move on to the device page section.

<center><img src="https://raw.githubusercontent.com/ArrowOS/blog/arrow/_assets/images/devices-d.PNG"></center>

This is how it looks like when you select a device, as you can see there are a bunch of features and options. Here's a brief description on what each of the options stand for:

<b>Weeklies</b> toggle: This indicates whether you want your device to be built for the next official weekly or if you want to opt-out(skip) your device from next weekly. A contributor is only allowed to skip 3 weeklies consecutively, after which his account will be disabled and locked out from configs temporarily until any further actions from the core members.

<b>"Path of repos to delete!" AND "Url's of repos to clone/sync!"</b>: This is generally for when you want to test something from a different branch or a different repository. Lets say i forked android_device_xiaomi_beryllium and made some changes which I want to test before pushing to ArrowOS-Devices org.
I will put device/xiaomi/beryllium into "Path of repos to delete!" textfield and My forked repository git link with path i.e device/xiaomi/beryllium with the branch were i made changes, in this case: staging-changes

<b>Repopick topics!</b>: To pick a topic from our gerrit/codereview for your device's build.

<b>Repopick change numbers!</b>: To pick commits from our gerrit/codereview using change numbers for your device's.

Now, moving further..

<center><img src="https://raw.githubusercontent.com/ArrowOS/blog/arrow/_assets/images/devices-d2.PNG"></center>

<b>XDA thread link:</b> This is where you link your XDA thread of your device, leave it empty if you have not posted in XDA forum yet. You can also post in other forums and ask the CORE team if you can link that instead. We may surely allow you.

<b>Changelog:</b> This is where you define your device specific changelogs, this will be shown on our [downloads page](https://arrowos.net/download.php)

<b>Push button</b>: really? haha. This will save your changes but won't initiate a build compilation.

<center><img src="https://raw.githubusercontent.com/ArrowOS/blog/arrow/_assets/images/devices-d3.PNG"></center>
These do what they say they do. Build -> builds, Abort -> aborts etc, nothing fancy.

<b>NOTE:</b> <br>
* Build button will once again save your existing changes before initiating a build compilation.
* When WEEKLY builds are running, all contributors access to the build section will be locked out.
* Before every OFFICIAL WEEKLY or OFFICIAL BUILD CYCLE, it is the responsibility of the contributor to clear their test config changes if any and update device changelogs frequently as you see fit.
* You can use configs to make test builds anytime, as many times as you like. If there's already a build running in the node assigned for your device, it'll be queued.
* When you toggle "Boot Image" switch, it will only compile a boot.img

The builds compiled by a contributor goes to our [experimental builds org in sourceforge](https://sourceforge.net/projects/arrowos-experiments/)

#### Stay home, Stay safe!

#### Want to contribute? and one day earn a spot in the CORE team? <br>

[Checkout this post](https://blog.arrowos.net/posts/apply-for-maintainership)

###### Write to us about your thoughts at <arrowos.contact@gmail.com> and in the comments section below. <br>