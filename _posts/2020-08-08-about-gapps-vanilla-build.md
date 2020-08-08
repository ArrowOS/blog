---
layout: post
title: "Detailed Information about our GApps and VANILLA build types; Recent changes on GApps builds"
description: "All info about our official gapps builds"
thumb_image: "https://raw.githubusercontent.com/ArrowOS/arrow_logos/master/ArrowLogo-sky-transparent.png"
priority: 1001
tags: [arrowos, android, news, gapps]
---

Published on: Aug 08, 2020 by Michael P, Kuber Sharma<br>

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

<span class="Dropcap">H</span>ello, аfter some  internal discussion, we decided to make GApps build with full-fledged built-in gapps. It includes G-Play services and now some AOSP apps have been replaced with GApps. <br>So, as you know we have two types of builds <br><b>VANILLA</b> and <b>GAPPS</b>.

<b>Firstly</b>, a little bit about <b>VANILLA</b> builds. This are without GApps (clear AOSP). Ideal for those who like MicroG, wants to use without  GApps or likes to use his own preferred GApps package.

<b>Secondly</b>, I will inform you about <b>GAPPS</b> builds and the recent changes that will reflect on them from next weekly.

What it includes now and what are the changes, you ask?

Below are the GApps that will be shipped and will override AOSP alternatives in GApps build now:

* Play Services, Core apps and Play Store
* Dialer
* Messaging
* Contacts
* Calculator
* Calendar
* Clock
* Sound Picker
* Device Personalization Services with Live Caption and etc.
* Keyboard
* Android System WebView

All similar <b>AOSP apps have been overwritten with GApps</b>. You don't have to delete or freeze them manually.

All GApps packages and another files extracted from original firmware images for Pixel4XL (coral).

Why didn't we add more apps? You can install them yourself using Play Store. We want to give the user the maximum choice.

GAPPS builds are only available for devices with an official status.

#### Revamped downloads page is live now<br>
As we mentioned in our [previous post](https://blog.arrowos.net/posts/www-thenewcoreguy), our downloads page is now dynamic and revamped. You should check it out to download the latest build for your device, [click here to open it](https://arrowos.net/download.php)

#### Want to become official maintainer?<br>

[Checkout this post](https://blog.arrowos.net/posts/apply-for-maintainership)

###### Write to us about your thoughts at <arrowos.contact@gmail.com> and in the comments section below. <br>

