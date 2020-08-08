---
layout: post
title: "Briefing about our Infra, Team and internal configs platform"
description: "How our infra and management evolved overtime"
thumb_image: "https://raw.githubusercontent.com/ArrowOS/arrow_logos/master/ArrowLogo-sky-transparent.png"
priority: 1002
tags: [arrowos, android, news, infra, team, configs]
---

Published on: Aug 08, 2020 by Ganesh Varma, Kuber Sharma<br>

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

<span class="Dropcap">A</span> steady progress is an integral part for any project and we here have been significantly growing over the span of time sharpening our skills, both as a developer and a multitasking juggler. We started the project with no interest of going big, but thanks to the community for showing us that there's a lot of you out there that look upon our work. When it all began we started as a team of 3, now we provide official support for various devices along with our contributors. (We like to address our device maintainers as contributors, they play a major role in the community bonding and project development).

#### Infrastructure <br>
Just like our team efforts the infra iterated over time with each android version. We now have a total of 3 build nodes up and running 24/7 free for the contributors to test and help in faster development cycles. For the ease of access and management of several builds daily going through our jenkins we recently worked up on a pipeline build structure with less clutter and better flow. This has significantly cut down our supervision over individual build jobs for any small changes on each device, which it used to be before. With the pipeline in place we further needed a easy to use and user firendly access platform to interact and initiate jenkins builds. This led to the birth of our configs platform.

#### Configs platform <br>
This acts as an interactive bridge between jenkins and the pipeline in handling independent device parameters via a neat web interface without the hassle of going through CLI. It has been put through test for more than half a year now and faired well among our contributors. With this platform in place it acts as a final piece in our management structure as it also acts as a portal for us admins to have a better overview of the progress.

Our infra is always under constant improvements to provide a better working environment. A deep breifing guide on configs will be shared soon on explaining its use and capabilities, and how it has helped in pushing out more refined builds by our contributors.

This has been a great journey soo far and glad to debrief everyone on what we have been doing in the background for the success of the overall project integrity. Community has always been our strong point, thanks for all of your constant support.

#### Stay home, Stay safe!

#### Want to contribute? and one day earn a spot in the CORE team? <br>

[Checkout this post](https://blog.arrowos.net/posts/apply-for-maintainership)

###### Write to us about your thoughts at <arrowos.contact@gmail.com> and in the comments section below. <br>