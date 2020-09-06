---
layout: post
title: "How to compile ArrowOS from source"
description: "guide on how to compile rom from source"
thumb_image: "https://raw.githubusercontent.com/ArrowOS/arrow_logos/master/ArrowLogo-sky-transparent.png"
tags: [arrowos, guide]
priority: 997
---

Published **July 12, 2018** by **Kuber Sharma, Bauuuuuu, Ganesh Varma**
Last updated on: **9th September, 2020** by **Kuber Sharma**

<center><img src="https://media0.giphy.com/media/3aGZA6WLI9Jde/giphy.gif"></center>

**So before we begin do checkout the below guides!**

[Establishing a Build Environment](https://source.android.com/setup/build/initializing)<br>
[Repo command reference](https://source.android.com/setup/develop/repo)<br>
[The Android Source Code & its structure](https://source.android.com/setup/)<br>

***Lets Begin***
<center><img src="https://media3.giphy.com/media/Axqr1hNEmGJiw/giphy.gif"></center>

##### **Initialize your local repository & Sync:**
{% highlight bash %}
mkdir arrow
cd arrow
repo init -u https://github.com/ArrowOS/android_manifest.git -b arrow-10.0
repo sync --force-sync --no-clone-bundle -j$(nproc --all)
{% endhighlight %}


**To maintain the quality of device sources we recommend using device Tree, device-common, kernel source, vendor from LineageOS/TheMuppets ORG thus this guide will be based on how to compile Arrow OS after adapting LineageOS Device sources to our platform**

##### **Adapting Tree to compile ArrowOS:**

**lineage_device-codename.mk -> arrow_device-codename.mk**

##### **Now inside arrow_device.mk:**
  - Change **"lineage" to "arrow" & /"common_full_phone.mk" to "common.mk"**<br> 
for e.g: $(call inherit-product, vendor/arrow/config/common.mk)
  - Change PRODUCT_NAME value **"lineage_device-codename"<br>
for e.g: ( "lineage_beryllium" ) to arrow_device-codename ( i.e, arrow_beryllium )**

##### **Dependencies:**
Rename "*lineage.dependencies*" to "*arrow.dependencies*". Add all your device dependencies in here (mainly common device repo, kernel repo, vendor repo or if any other like toolchain etc)

**Note:** The dependencies file is to be only placed in device repo that follows the following naming structure **android_device_<<manufacturer>>_<<codename>>** as the roomservice tool will only be looking into it.

**Here is a sample of the dependencies file**
{% highlight bash %}
[
{
"repository": "android_vendor_zuk_z2_plus",
"target_path": "vendor/zuk"
},
{
"repository": "android_device_zuk_msm8996-common",
"target_path": "device/zuk/msm8996-common"
},
{
"repository": "android_kernel_zuk_msm8996",
"target_path": "kernel/zuk/msm8996"
}
]
{% endhighlight %}

##### **Removing stuff related to Lineage SDK etc:**
It is necessary to clean up any specific files from LineageOS as these features depend on Los SDK which won't be available on AOSP and results in build failures.
**eg:** ***LiveDisplay, LineageParts, LineageOverlays, Lineage touch HAL etc.***

From the root of your device tree/Common device tree remove the following folders/files:
  - lineagehw
  - livedisplay
  - touch

Simillarly from **BoardConfig.mk/BoardConfigCommon.mk**:
{% highlight bash %}
# Lineage Hardware
BOARD_HARDWARE_CLASS += \
$(VENDOR_PATH)/lineagehw
{% endhighlight %}

From **manifest.xml** remove livedisplay HAL:
{% highlight bash %}
    <hal format="hidl">
        <name>vendor.lineage.livedisplay</name>
        <transport>hwbinder</transport>
        <version>1.0</version>
        <interface>
            <name>IColor</name>
            <instance>default</instance>
        </interface>
    </hal>
    <hal format="hidl">
        <name>vendor.lineage.touch</name>
        <transport>hwbinder</transport>
        <version>1.0</version>
        <interface>
            <name>ITouchscreenGesture</name>
            <instance>default</instance>
        </interface>
    </hal>
    <hal format="hidl">
        <name>vendor.lineage.trust</name>
        <transport>hwbinder</transport>
        <version>1.0</version>
        <interface>
            <name>IUsbRestrict</name>
            <instance>default</instance>
        </interface>
    </hal>
{% endhighlight %}

From **device.mk**(also named as your SOC codename like: **msm8996.mk**) OR **common.mk** incase of common trees:
{% highlight bash %}
DEVICE_PACKAGE_OVERLAYS += $(LOCAL_PATH)/overlay-lineage

# LiveDisplay native
PRODUCT_PACKAGES += \
    vendor.lineage.livedisplay*

# Touch
PRODUCT_PACKAGES += \
    vendor.lineage.touch*

# Trust HAL
PRODUCT_PACKAGES += \
    vendor.lineage.trust*

{% endhighlight %}

**Note:** There is possiblity that some custom packages such as doze etc may have dependency on lineageSDK, it is necessary to fix them to avoid complie errors.

For e.g: From **parts/AndroidManifest.xml** OR **doze/AndroidManifest.xml** in your device/common device source:
Remove the below line:
{% highlight bash %}
            <intent-filter>
                <action android:name="org.lineageos.settings.device.DOZE_SETTINGS" />
                <category android:name="android.intent.category.DEFAULT" />
            </intent-filter>
{% endhighlight %}
And set an overlay in **overlay/packages/apps/Settings/res/values/config.xml** inside your device/common device tree
{% highlight bash %}
    <!-- Device specific doze package -->
    <string name="config_customDozePackage">org.lineageos.settings/org.lineageos.settings.doze.DozeSettingsActivity</string>
{% endhighlight %}

**NOTE:** Package name has to match to whatever your devices uses!

**Additional sets for a device with FOD:**
Lineage devices with FOD uses a feature permission XML to advertise that that device uses FOD feature

If you closely look at the **device.mk/common.mk etc**, you may find this:
{% highlight bash %}
 # Permissions
PRODUCT_COPY_FILES += \
    vendor/lineage/config/permissions/vendor.lineage.biometrics.fingerprint.inscreen.xml:$(TARGET_COPY_OUT_SYSTEM)/etc/permissions/vendor.lineage.biometrics.fingerprint.inscreen.xml
{% endhighlight %}

This will cause a build error, so remove it.
As of arrow-10.0, you can implement FOD in case your device supports it by setting an overlay
inside your device tree: /overlay/frameworks/base/core/res/res/values/config.xml
{% highlight bash %}
    <!-- Shows the required view for in-display fingerprint -->
    <bool name="config_supportsInDisplayFingerprint">true</bool>
{% endhighlight %}

##### **To start the rom compilation:**
From the root of your source directory run the following commands
{% highlight bash %}
. build/envsetup.sh
lunch arrow_<devicecodename>
mka bacon
{% endhighlight %}

If the device is good for daily use, you can submit it to our [Community Devices](https://blog.arrowos.net/posts/community-builds-stay-tuned) and use our [infrastructure](https://blog.arrowos.net/posts/infra-jenkins-configs-platform) to benefit many other users for the same device, or if you have gained some knowledge, have some time to dedicate and pass the certain criteria to continously support the  device as an Official device and join the team you can [submit an application](https://blog.arrowos.net/posts/apply-for-maintainership)

<center><img src="https://media.giphy.com/media/NdTyWmj9mJgpq/giphy.gif"></center>
