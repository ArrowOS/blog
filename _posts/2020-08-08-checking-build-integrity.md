---
layout: post
title: "HOW-TO: Checking Build Integrity of our Official builds"
description: "We explain how to you can check build Integrity of our builds."
thumb_image: "https://raw.githubusercontent.com/ArrowOS/arrow_logos/master/ArrowLogo-sky-transparent.png"
priority: 1001
tags: [arrowos, android, news, integrity]
---

Published on: Aug 08, 2020 by  Kuber Sharma<br>

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

<span class="Dropcap">H</span>ere is how you can get sha256 of the latest ArrowOS build that you downloaded and match it with the sha256 we are displaying on our [downloads page](https://arrowos.net/downloads.php)

###### Windows

{% highlight bash %}
Get-filehash Arrow-*.zip
{% endhighlight %}

<center><img src="https://raw.githubusercontent.com/ArrowOS/blog/arrow/_assets/images/sha256-win10.PNG">Windows 10 - Powershell</center>

###### Linux
{% highlight bash %}
sha256sum Arrow-*.zip
{% endhighlight %}

<center><img src="https://raw.githubusercontent.com/ArrowOS/blog/arrow/_assets/images/sha256-linux.PNG">Ubuntu 20.04 LTS</center>

<b>NOTE:</b> "Arrow-*.zip" is the build that you have downloaded.

You can get see the sha256 of official builds [here](https://arrowos.net/downloads.php) - Remember to select your device and lookout for your preferred the build type i.e VANILLA or GApps


###### Write to us about your thoughts at <arrowos.contact@gmail.com> and in the comments section below. <br>

