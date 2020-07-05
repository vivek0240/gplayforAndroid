This package is designed for users of legacy devices with small system partitions or those who prefer a minimalistic approach.
In this package you will find the core Google system base, Google Android Shared Library, Google Play Store, **Google Exchange Services _(replaces stock/AOSP Exchange Services)_**, Face Detection for Media, Dialer Framework and the following Play Store applications:

* Device Health Services
* **Gmail**
* Google App (Search)
* **Google Calendar _(replaces stock/AOSP Calendar)_**
* **Google Pixel Launcher**
* Google Package Installer _(replaces stock/AOSP Package Installer)_
* Google Play services
* Google Text-to-Speech
* Google Wallpapers
* Pixel Icons

For 6.0+ also:
* Google Text-to-Speech

For 9.0+ also:
* Google Sounds
* Google Digital Wellbeing

Notes:
* Bold apps mark the difference to smaller packages.
* Google removed the `Trusted Face` (FaceUnlock) feature for security reasons (see [this post](https://www.androidpolice.com/2019/09/04/trusted-face-smart-unlock-method-has-been-removed-from-android-devices/)). We've removed the corresponding code for the `FaceDetect` and `FaceUnlock` for all platforms.