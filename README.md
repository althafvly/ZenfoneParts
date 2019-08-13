# How to add ZenfoneParts to your Device Tree

First clone this repo in your Device Tree folder by doing -

`git clone https://github.com/saurabhchardereal/ZenfoneParts.git`

### Then check your ROM source for KeyHandler to match the one present in ZenfoneParts

To do this just go to your respective ROM's **platform_frameworks_base** repo and navigate to **core/java/android/provider** and open up **Settings.java** search for `DEVICE_PROXI_CHECK_ENABLED`

If the above phrase is as it is then you dont have to edit it in ZenfoneParts but if it's something different, like for example in Bootleggers ROM it is `OMNI_DEVICE_PROXI_CHECK_ENABLED` then you have to replace `DEVICE_PROXI_CHECK_ENABLED` line to `OMNI_DEVICE_PROXI_CHECK_ENABLED` from **ZenfoneParts/src/com/asus/zenparts/KeyHandler.java** and **ZenfoneParts/src/com/asus/zenparts/settings/DeviceSettings.java**

You have to do the exact same for `BUTTON_EXTRA_KEY_MAPPING`

### After doing all that just cherry-pick or merge the below commit to enable support for ZenfoneParts

https://github.com/travarilo/device_asus_X00T/commit/e3f05754dd1b066749951529091a843bec1bdcea

### And that's it! You have successfully added ZenfoneParts to your DT


**All credit goes to _@travarilo_ and _@Genkzsz11_ for ZenfoneParts!**
