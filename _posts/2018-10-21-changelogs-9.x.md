---
layout: post
title: "Changelogs 9.x(PIE)"
description: "This post is updated regularly || Last updated on: 13th June, 2019"
thumb_image: "https://raw.githubusercontent.com/ArrowOS/arrow_logos/master/ArrowLogo-sky-transparent.png"
tags: [arrowos, changelog, pie]
priority: 999
---

## ArrowOS Changelogs for 9.x(PIE)

Published on: July 28, 2018 by Kuber Sharma, Bauuuuu, Ganesh Varma, Amitava Mitra<br>
Last updated on: 13th June, 2019

## Important Note
This post is updated whenever there are any new updates!

#### DOWNLOADS
All the builds for official devices can be found [here](https://sourceforge.net/projects/arrow-os/files/arrow-9.x/)

#### COMMUNITY
[Telegram Chat](https://t.me/arrowos)
[Telegram Channel](https://t.me/arrow_os)

You can find changelogs for Arrow-8.x(Oreo) [here](https://blog.arrowos.net/posts/changelogs-8-x)

## CHANGELOGS

### 12th June, 2019
* Merged latest Aosp tag/June security patch
* Added CircularStd font
* Sepolicy update
* Misc fixes, updates and more(Check more in gerrit)

# Following devices are dropped due to inactive maintainers:
cedric, platina

### 17th April, 2019

- Added support for Framework Boost ( for selective devices only )
- Added Aggressive Battery Saver Mode
- Toast related theme fixes
- Added AOD tile (specific devices only)
- Some Phonograph Music player fixes
- Added Deep Sleep info in System uptime
- Fixed no service and emergency calls only placement 
- Added support for .opus file extension
- Reduce some unnecessary logspam
- Fix EmergencyDialer showing in recents
- Media/Ringtone gesture toasts now get themed with system theme (Dark/White)
- Fonts: Add Roboto Condensed and SanFrancisco Pro
- Other: bug fixes, improvements / minor updates  etc can be seen in gerrit ( review.arrowos.net )

### 26th Mar, 2019 
- Ambient music ticker AoD: make it compatibile with double tap sensor
- Ambient music ticker: play nice with omni weather
- Ambient Display Music Ticker: Nuke song count info
- Ambient Music Ticker: make it pixel like 
- Fix lockscreen double tap to open notifications after ambient music
- Screen off to skip track: Add Spotify/KDEConn/etc. 
- Snap: Fix picture size preference 
- Ambient display music ticker 
- Turn on display if Doze On Charge is Enabled 
- dynamic arrow indicators for statusbar network traffic 
- expandable volume panel
- TrafficSB: Hide arrows in statusbar traffic indicators 
- Added font service
- invictrix fonts & statix fonts (Settings->Display->Font)
- Added 3 mode disply cutout (Settings->Display->display cutout settings)
- DocumentsUI: white navbar for DocumentsUI
- Translations Updated
- minor bugfixes and improvments (visit gerrit or github org)

# Following devices are dropped due to inactive maintainers:
vince, tissot, kenzo

### 14th Mar, 2019 
- Android security patch March (r34)
- OOS style network traffic indicator
- Individual toggles for QS and statusbar traffic indicators
- systemui: reduce padding between signal icons and battery
- BatteryMeterView: Fix logcat spam
- Use normal tinting for emergency icons
- fix status bar mobile view layout problem
- Improve performance of unclipped save layers.
- Fix flickering issue when live wallpaper is showing on aod
- wake from aod on unplug if we show on charging only
- Dash charging: Add the battery percent back
- Re-add WPS implementation
- Fix summary text for advanced button
- Settings: Bring back Uptime
- Settings: show battery times in summary
- Settings: enable SIM card ringtone only if slot not empty
- replaced Simple gallery with AOSP Gallery
- Automatic translation imports
- Fix carrier config option not hidden on a CDMA phone
- NfcNci: make T3T/Nfc-F HCE optional
- Fixed tinting for emergency icons
- Fixes to elliptic ultrasound devices (device specific)
- removed teal color from the default printer service
- Use GoogleSans on package installer app title
- Updated search bar style on dark theme
- DocumentsUI: Improve dark theme
- DocumentsUI: Fix navbar themeing
- DocumentsUI: support night mode
- Translations Updated

# New devices added:
chiron(Xiaomi Mi Mix 2) - @Perfectime94
platina(Xiaomi MI 8 Lite) - @melvingarcia
# Builds are available on sourceforge already, OTA will be available within 24hrs!!!

### 14th Feb, 2019 
- Merge February Security patch(r31)
- new Volte icon extracted from asus Pie beta
- Fixed signature spoofing support
- Hide arrows in Network Traffic indicators
- Move statusbar weather to QS statusbar header
- Move net monitor to expanded statusbar header
- Make weather clickable in QS status bar header
- Make traffic clickable in QS status bar header
- Make statusbar header net monitor play nice with the QS Scrim
- Clear all lingering notifications when network is disconnected
- Remove unnecessary right padding from time picker
- Network traffic: fix indicator not hiding on lost connection
- Net monitor: fix text color on light theme
- Statusbar net monitor: stop the handler if screen is off
- SystemUI: Ambient Display: fixed overlap of  weather and notifications
- Fix disappearing home/recents button
- Translations Updated
- Updated qcom hals
- optimisations, core changes and fixes which is not mentioned here but can be seen at Github Org or Gerrit

New Devices : Motorola One Power (chef), Smartron srt (rimo02a), Motorola G5 (cedric)
Dropped Devices: Xiaomi Mi A1 (tissot)
# Builds are available on sourceforge already, OTA will be available within 24hrs!!!

### 28th January, 2019
- Fixed weather not getting updated 
- Keyguard weather styles, option to display weather and conditions in one line
- Removed Yahoo weather provider
- Option to add Custom API key for OpenWeatherMap
- Added Navigation Bar QS Tile toggle
- Moved out buttons and navbar option to dashboard
- Fixed signature spoofing (microG)
- FMradio: fixed crash when adding radio station to favorites
- Display Dash charging for dash charge in battery settings(oneplus devices)
- Fix mediascanner access permissions to external storage 
- Make keyguard weather icon smaller
- Hide check button when using PIN quick unlock
- Auto face unlock v2 for pie 
- Unconditional led notifications for dialer and many other apps
- Translation update for several apps

### 12th January, 2019
- Merged android-9.0.0_r30 tag (Jan security patches)
- Fix unlinked ringtone and notification volumes panels
- Make installer header look a little better
- Show a more descriptive message when vendor.img is out of date
- Snap camera updates and fixes
- Only show bluetooth icon when connected & enabled
- Don't crash if there is IR HAL is not declared
- Packages like Camera2, Email, UnifiedMail, Exchange are updated,
- Volume slider related fixes
- Some layout changes in Sound Settings
- Fixed Settings force close when searching for second time,
- Fixed a crash for bad package name,
- Translations
- several of optimizations, core changes and fixes

### 8th December, 2018
From last few weeks team discussions we're bringing in few changes to our weeklies startegy.The weeklies now will be moved to bi-weeklies. Which means there will be update after the android security bulletin starting each month and the second update will be within next 10-14 days of first update. Overall two updates per month. We are at this stage that the changes to source are not very dynamic as compared to early PIE release days, rather pretty stable. This is to give us and the maintainers more firm control over the changes being introduced and enough time to test them out for a more refined and stable update to our users. Having written that, the critical updates related with specific device will be released as and when required. Moreover, from our stats we are noticing that few devices still have huge userbase on ArrOW Oreo and hence for these devices we will provide the Oreo updates with latest securrity patch merged and misc fixes.

Android Security patch Level : 5 Dec 2018
- Option to unlink ringtone and notification sound
- Keymaster updates
- Fix high battery drain after using flashlight
- DownloadProvider: allow more redirects
- DownloadProvider: ability to pause/resume downloads
- Prevent crash when multiple Screenshot request is made
- LatinIME: Fix dicttool build
- Latin IME bug with deleted text will reappear after screen orientation changes
- Fixing layouts and adding 5th row to QWERTZ
- LatinIME: Fix to English dictionary can be added after deleting
- Add 5th number row to keyboard.
- Launcher: Add back button to Settings 
- Launcher: Move package icon to the end if the preference 
- Translations 
- Rremoved Turbo
- device related fixes, kernel upstream

### 1st December, 2018
- Updated DeskClock, also added support of power off alarm feature (Device dependent).
- Changed default animation scales to x0.8.
- Optimisations for faster animation speeds.
- Animation scale can be tweaked using a seekbar.
- Added a toast when screenshot is deleted
- Prevent crash when multiple Screenshot request is made
- Expose screenshot flash colors for themes
- Fixed too big spacing between QS icons in landscape on sw600dp 
- Import updated APNs from Google.
- Fixed: removed duplicate alarm sounds.
- Updated translations.
- Added Reboot and Recovery QS tile.
- Added Night Light brightness mode options.
- Fixed: DnD tile long-press.
- Quickstep: added Rounded square icon shape.
- Quickstep: App Apps search bar has rounded corners.
- Removed: QS panel Opacity 
- Fixed screen saver FC due to missing flag 
- touch response optimizations 
- Other changes: core optimisations, device side changes. More info can be seen on gerrit.

### 25th November, 2018

-  Add new feature of One-hand UI Mode
-  Statusbar battery level device filter: add a few more ones
-  SystemUI: Show bluetooth battery level when available
-  Automatic translation import
-  fwb: Implement alternative device key handler
-  base: add settings for device features
-  BurnInProtection: Fix null object reference with timer
-  Do not move the multi-window divider when showing IME
-  Fix StatusBar icons tinting when in split screen
-  Framework: Remove some methods from boot image profile
-  SystemUI: Fix mCallbacks is not thread-safe
-  Synchronize mPermissions to void NullPointerException
-  Remove NotificationVisibility storage pool
-  Keyguard: Remove carrier text for disabled SIMs
-  SignalClusterView: Hide signal icons for disabled SIMs
-  Refusing to enter PIP mode when activity destroyed
-  Fix PIP media session listener for secondary users
-  Fix the behavior of keyguard bouncer in a corner case
-  SystemUI: Fixes context for tiles without longClick
-  ActivityManager: Fix display id JE issue
-  am: Fix top activity resume with secure keyguard
-  Delay blanking of displays to improve performance
-  Fix intermittent slowness in resolver activity towards end of day
-  Other changes: core optimisations, device side changes. More info can be seen on gerrit

### 18th November, 2018
- Add Custom Icon Pack support
- Swipe down gesture support on Launcher
- Configurable App title lables in drawer and homescreen
- Add support for ringtones per sim
- Translations by community merged
- Messaging app updates, pixel color default
- Long touch on  QS Title will show detailed view
- Fixed QS Tiles title visibility
- Qcom HAL upates
- VoLTE icon from OOS Pie
- Other changes: optimisations, core changes, package updates etc. More info can be seen on gerrit

### 11th November, 2018
 - November security patch r16.
 - Longpress power for torch on lockscreen.
 - Full navbar gestures (swipe left for back action).
 - Double tap on navbar to sleep.
 - Toggle to set QS brightness slider on bottom.
 - Toggle to completly disable brightness slider from QS panel.
 - Full FDE (encryption) support. (device specific)
 - Option to set separate ringtones for mutilple sims.
 - Latest translation changes.
 - many more upstream changes & fixes.
 - Device related fixes and kernel upstream

### 2nd November, 2018
  - New Spooky Bootanimation (Halloween Special)
  - Spooky Halloween notification sounds (Halloween Special)
  - Halloween wallpaper (Halloween Special)
  - Themed to Halloween orange accent by default (Halloween Special)
  - Added spooky Halloween ringtone & alarm sound by default (Halloween Special)
  - Added spooky SeLinux status message (Halloween Special)
  - Fixed battery charging indication bug 
  - Secure QS tiles when the device is locked (requires unlocking to use quick tiles)
  - Added Recorder app 
  - Themed package installer
  - Added all pixel & pixel 2 sounds
  - Added Google’s new alarm sounds
  - Added Audio and Screen recorder
  - Added Google nexus audio files
  - Made batterysaver dark mode state configurable 
  - Lockscreen charging indication fixed 
  - Disabled Hungarian spell checking
  - Add Luxembourgish keyboard & spellchecking dictionary
  - Fixed battery settings fc 
  - SDClang optimizations 
  - Enabled Smart notification reply for supported apps
  - Some string improvements for better user understanding
  - Updated Translations
  - And many more core optimizations & fixes
  
### 28th October, 2018
  - VoLTE icon
  - VoLTE icon enable and disable switch.(disabled by default)
  - Added location tile cycle modes
  - Added arrowos default wallpaper
  - Fixed night mode to work on light theme
  - Added hide signal icons for disabled sims  
  - Fixed usbdevicemanager null object reference  
  - Added screen unpinning on devices without navbar
  - Notification light switch hide pref on no config
  - Removed night mode from developers settings  
  - Moved battery light settings into dashboard battery section
  - Swipetonotificationsettings: added proper check on search index
  - Fixed ghost toggling of night mode
  - Fixed NPE of battery settings
  - Refactored ArrowOS preference in About into Firmware dialog.
  - Also added info for build date, and official status of the rom.
  - Fuelgauge optimisations for better and accurate battery stats.
  - Re-arranged density, display and font size options to their own category(Desity options).
  - Added screenshot QS tile.
  - Added translations
  - Upstream changes
  - And many more core optimizations & Fixes

### 21st October, 2018

  - Merged tag 'android-9.0.0_r12' 
  - Fixed initial value of qs columns to default aosp 
  - Added phonograph 
  - Add NightMode under display SystemUI theme category 
  - Added config to disable cdma call forward/waiting 
  - Added conference uri support 
  - Added support for implicit call rejection
  - Added avoid wifi to cellular silent redial when roaming 
  - Added config to control holding a video call 
  - Added get sim card capacity count of sms 
  - Added allow emergency ims network request in sim less case 
  - Updater will generate changelog url dynamically 
  - Updated pixel colors from taimen 
  - Added fingerprint authentication vibration 
  - Added unlock keystore with fingerprint after reboot 
  - Added Expanded Desktop
  - Fixed preferred calls sim not being disabled 
  - And many more core optimizations & fixes

### 14th October, 2018

  - Added lockdown on power menu & its lockscreen visibility
  - Power menu tracks accents now
  - Option to disable QS footer warnings
  - Autobrightness toggle on QS
  - updated NFC QS tile and statusbar icon
  - fix facelock crash when lock screen is disabled
  - Show Auto-BT while driving setting
  - Pixel navbar animation
  - Dual Channel into Bluetooth Audio Channel Mode
  - Materialize Toast notifications
  - batterysaver ring on circle battery icon
  - Camera2 fixes and improvments
  - Misc bug fixes & improvements
  - Add switches to show city/temp on lockscreen
  - allow to swipe down on recents view to clear all default launcher
  - Google Feed integration on default launcher
  - Allow resizing any widget on default Launcher
  - Updated Translations (Thanks to community)
