# LADB
A local ADB shell for Android!

## Overview
LADB is undled with an pre-compiled ADB library modified
for the Android architecture. It functions as a bridge connecting the device
to a localhost server without the need for a separate device!
This means that LADB can send `adb shell` commands
as if they were being executed from a host PC with USB-Debugging enabled.
With that in mind you now have more control over your device!


### Initial Setup:
**1. Enable Developer Mode**
 - **About -> Build Number -> Click 7 times**

**2. In Developer Settings**
 - Wireless debugging -> On
 - USB Debugging -> On

#### Notes:
- Android 12 seems to have broken the app on select devices.
See issue [#62](https://github.com/tytydraco/LADB/issues/62)
----
### Troubleshooting:
<details>
<summary>Device unauthorized/Multiple devices connected</summary>


   1. Detach any devices
   2. Force stop LADB(see use case below)
   3. Enable/Disable Airplane Mode
   4. Goto step 2 of [Initial Setup](#initial-setup)

----
</details>

#### Still having connection Problems?

**1. Force stop LADB**
  - _(Eg.
**Settings -> Apps -> LADB -> Force Stop**)_

**2. In Developer Settings**
  - Wireless debugging -> Toggle Off
  - USB debugging -> Toggle Off
  - Revoke USB debugging authorizations
  - Reboot

**3. Again in Developer Settings**
 + USB Debugging -> On
 + Wireless debugging -> On

**4. Open LADB and follow the prompts!**

#### Can't Split Screen Settings App?

 - Goto **Settings -> Developer Options -> Force Allow Apps Resizable**
See issue [#57](https://github.com/tytydraco/LADB/issues/57)

**NOTICE:**
_Some of the Settings labels may differ depending on your
phones model and Android version. As of writing this
I'm using stock AOSP Android 11 - NonstickAtom_


----

# Credit
Thanks to [Surge1223](https://github.com/Surge1223) for compiling ADB for the ARM/ARM64 architecture.

# License
While this project is GPLv3 licensed, I would like to add an additional parameter: please do not publish unofficial (user) LADB builds to the Google Play Store.

Still confused? Email me at tylernij@gmail.com.
