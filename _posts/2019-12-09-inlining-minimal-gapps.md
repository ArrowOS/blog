---
layout: post
title: "Information regarding the inclusion of Minimal Google Apps (Services, Play Store etc) into the official builds!"
description: "All about inlining GApps into official builds."
thumb_image: "{% asset 'logo.png' @path %}"
priority: 1001
tags: [arrowos, android, news, gapps]
---

Published on: Dec 08, 2019 by Kuber Sharma, Bauuuuu, Ganesh Varma<br>
Updated on: Dec 16, 2019 by Ganesh Varma, Regarding non-gapps version conclusion<br>

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

<span class="Dropcap">W</span>ith some recent internal discussions regarding GApps packages the team has come to a conclusion of maintaining it's own fork of GApps which will be shipped in with the official builds. This being very minimal doesn't have any drastic increase in the zip size and overall provides a fair and lite usage for accessing Google services right from your first clean boot.

# F.A.Q <br>
#### Q: What made you inline gapps?

A: With the lack of official opengapps for android-10 and in a growing increase of complaints from people breaking their boot by flashing several versions of gapps that are available out in the community we find it as a much more needed necessity to inline our own minimal version of gapps.

We always strive to provide a clean and hassle free experience right from the initial boot of the rom. Hoping that this makes things cleaner in those initial flashing stages without the need to flash additional gapps zips anymore and keeping things stable on a common version of gapps overall our official devices.

#### Q: Will i still be able to flash OpenGapps? (**Not recommended**)

A: Yes, but the opengapps package you used has to be flashed on along with every update of the rom. 

#### Q: Will there be a non gapps version releases? [UPDATE - 16/12/2019]

~~A: This is still an ongoing discussion and we would like to hear your thoughts on this.~~<br>

A: Yes, we have concluded to ship two versions. The non-gapps version zips will be named as **VANILLA** while the gapps version zips will be named **GAPPS**. Updates for both versions will be pushed on the same day. The OTA Updater will manage to receive and install the updates according to the version you're on.

#### Q: Will i be able to switch between two versions?

A: Switching between the two types with a dirty flash is not recommended at all. Also the Updater won't be providing any functionlity to switch between two versions and we don't encourage anyone to do so. As long as you do a clean flash it'll be fine to switch between vanilla and GApps versions.

###### Write to us about your thoughts at <arrowos.contact@gmail.com> and in the comments section below. <br>