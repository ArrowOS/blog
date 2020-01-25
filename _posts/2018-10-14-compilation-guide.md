---
layout: post
title: "How to compile ArrowOS from source"
description: "guide on how to compile rom from source"
thumb_image: "{% asset 'logo.png' @path %}"
tags: [arrowos, guide]
priority: 997
---

Published July 12, 2018 by Kuber Sharma, Bauuuuuu, Ganesh Varma

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
repo init -u https://github.com/ArrowOS/android_manifest.git -b arrow-9.x
repo sync  -f --force-sync --no-clone-bundle -jX
{% endhighlight %}
Where X in the above command is no.of threads your CPU can handle.

**To maintain the quality of device sources we recommend using device Tree, device-common, kernel source, vendor from LineageOS thus this guide will be based on how to compile Arrow OS using LineageOS Device Trees**

##### **Adapting Tree to compile ArrowOS:**

**lineage.mk -> arrow.mk**

##### **Now inside arrow.mk:**
  - Change **"lineage" to "arrow" & /"common_full_phone.mk" to "common.mk"**<br> 
for e.g: $(call inherit-product, vendor/arrow/config/common.mk)
  - Change PRODUCT_NAME value **"lineage_device-codename"<br>
for e.g: ( "lineage_mido" ) to arrow_device-codename ( i.e, arrow_mido )**

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
**eg:** ***LiveDisplay, LineageParts, LineageOverlays etc.***

From the root of your device tree/Common device tree remove the following folders/files:
  - lineage-overlays
  - lineagehw

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
{% endhighlight %}

From **device.mk**(also named as your SOC codename like: msm8996.mk):
{% highlight bash %}
DEVICE_PACKAGE_OVERLAYS += $(LOCAL_PATH)/overlay-lineage

# LiveDisplay native
PRODUCT_PACKAGES += \
    vendor.lineage.livedisplay@1.0-service-sdm
{% endhighlight %}

**Note:** There is possiblity that some custom packages such as doze etc may have dependency on lineageSDK, it is necessary to fix them to avoid complie errors.

##### **To start the rom compilation:**
From the root of your source directory run the following commands
{% highlight bash %}
. build/envsetup.sh
lunch arrow_<devicecodename>
brunch <devicecodename>
{% endhighlight %}

<center><img src="https://media.giphy.com/media/NdTyWmj9mJgpq/giphy.gif"></center>
