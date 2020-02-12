* See [Notes for Android 10.x](https://github.com/opengapps/opengapps/wiki/Notes-for-Android-10.x) about the packages available @ the present for Android 10+.
* Google removed the `Trusted Face` (FaceUnlock) feature for security reasons (see [this post](https://www.androidpolice.com/2019/09/04/trusted-face-smart-unlock-method-has-been-removed-from-android-devices/)). We've removed the corresponding code for the `FaceDetect` and `FaceUnlock` for all platforms.

The Aroma package is a special version of the regular [['Super'|Package-Comparison]] package, but with a graphical front-end that will allow you to select which specific applications to install (or not) without having to manually write a [[gapps-config file|Advanced-Features-and-Options]]. Note: For versions of 5.0 and lower the Aroma package is based on Stock, and not all options shown are actually available within the package.
This package has a [dedicated thread at XDA](http://forum.xda-developers.com/android/general/open-gapps-aroma-installer-t3010798).

Screenshots of each step of the installation process are located [here](http://imgur.com/a/gBfR6)

# Issues
AROMA has some known issues, which vary by device and recovery version.

## Galaxy S5 (klte family)
* Affects models: SM-G900AZ, SM-G900F, SM-G900M, SM-G900R4, SM-G900R7, SM-G900T, SM-G900V, SM-G900W8, SM-S902L, SM-G870F, SM-G9006V, SM-G9008V, SM-G9006W, SM-G9008W, SM-G900FD, SM-G900MD, SM-G900I, SM-G900P, SCL-23, SM-G900K, SM-G900L & SM-G900S.
* Known broken TWRP versions: 3.3.1-0 (Crashes TWRP), 3.2.3-0 (Crashes TWRP), 3.2.1 (Crashes TWRP), 3.0.2-2 (Crashes TWRP), 2.8.4.0 (Doesn't install everything you select)

## OnePlus One (bacon)
* Known working TWRP versions: 2.8.4.0 
* Known broken TWRP versions: 2.8.7.0, 2.8.6.1, 3.0.0.1

## OnePlus X (onyx)
* Known broken TWRP versions: 3.0.2-0

## Moto X 2014 (victara)
* Known broken TWRP versions: 3.0.2-2 (crashes TWRP and forces reboot into system)

## Moto G (falcon)
* Known broken TWRP versions: 3.0.0.1

## Xiaomi Redmi Note 7 Pro (violet) & Xiaomi Redmi Note 7
* Users reported a device architecture error in bug report [#757](https://github.com/opengapps/opengapps/issues/757)