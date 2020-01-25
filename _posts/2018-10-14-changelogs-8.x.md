---
layout: post
title: "Changelogs 8.x(OREO)"
description: "This post is not updated anymore [DISCONTINUED], please refer to newer version"
thumb_image: "{% asset 'logo.png' @path %}"
tags: [arrowos, changelog, oreo]
priority: 995
---

## ArrowOS Changelogs for 8.x(OREO)

Published on: July 28, 2018 by Kuber Sharma, Bauuuuu, Ganesh Varma, Amitava Mitra<br>
Last updated on: 14th October, 2018

## Important Note
This post is updated whenever there are any new updates! 

#### DOWNLOADS
All the builds for official devices can be found [here](https://sourceforge.net/projects/arrow-os/files/arrow-8.x/)

#### COMMUNITY
[Telegram Chat](https://t.me/arrowos)
[Telegram Channel](https://t.me/arrow_os)

## CHANGELOGS
### 07th October, 2018
  - Add full OMS support ( rootless substratum )
  - Merged OCTOBER security patches!

### 25th August, 2018
  - August Android Security Patch
  - Frameworks: add ability to disable bar color in battery saver mode
  - Stop using rssnr, it falsly shows wrong signal bars
  - fwb: Add check for odm version
  - Add back button to demo mode fragment
  - Location: Skip processing when reciever pointer is null
  - fix synchronization bug when notification enqueue/cancel
  - core: ChooserActivity: fix android crash from null object
  - Remove unused calling for better performance
  - core: Fix long overflow issue in NetworkStats
  - MtpDatabase: Fix potential NULL dereference errors
  - Fix a 'memory leak'
  - Check for null path in getInternalPathForUser
  - ScanRecord.getServiceData NPE fix
  - Speed up the speed of computer MTP query
  - Fix problems caused by multithreading in VibratorService
  - Ensure battery saver preference is truly disabled while plugged
  - Fix NullPointerException in BatteryUtils
  - Avoid NullPointerException when updating preference intents
  - Fix settings force close
  - Fix for battery item summary that disappears
  - Fix for NPE caused by missing argument in setResult for ChooseLockGen
  - Fix the crash caused by show DialogFragment after it state already saved
  - Fix NPE crash in AppInfoBase
  - Fix the format of wifi_carrier_content string
  - Fix Phone Info FC
  - App notification config reset should also reset legacy notification
  - Settings: FC when rotate in Wifi AP detail page
  - Keep access point list updated once in short time.
  - Setting:BugFix for OOM caused by looper leak in settings
  - InstalledAppDetails: Avoid crash caused by ActivityNotFoundException
  - settings: bt: Fix NPE with switch state
  - Fix NPE in AutoSyncWorkDataPreferenceController
  - settings: update switch state only if there is change
