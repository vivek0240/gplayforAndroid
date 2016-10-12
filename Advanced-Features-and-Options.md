Advanced Features and Options
===
The features outlined below are COMPLETELY OPTIONAL and designed to allow advanced users the ability to modify the default behavior of the Open GApps installers. Without the use of these options, the installers will function exactly as described in [[Package Comparison|Package-Comparison]] chart.

The gapps-config file
---
To modify the default behavior of the Open GApps installer, create a text file called **.gapps-config** or **gapps-config.txt** (.gapps-config will take precedence) and place it in the **same folder as the Open GApps zip** or in **/sdcard/Open-GApps** or in **/persist** (within zip's folder will take precedence). Once you've created the gapps-config file, simply type in the keyword options you want from the lists below. There is also a more user-friendly front-end available that can generate the gapps-config file for you behind the scenes: the [[Aroma Package]]

####Config files per device
If you want to use different settings per device, you can create a text file named **.gapps-config-devicename** or **gapps-config-devicename.txt** replacing **devicename** with your device's codename (which is also shown in _open\_gapps\_log.txt_) and put it in the same locations described above. (You can usually find it in the name of your ROM download). If you don't provide one, the normal gapps-config file will be used.

####Testing
To perform a test installation that will only simulate an install, add the keyword `Test` to your gapps-config. The installer will perform all system space calculations and generate a detailed _**open\_gapps\_log.txt**_ (in the same folder as your gapps-config), but WILL NOT MAKE ANY CHANGES to your device. This should be helpful for trying to find just the right combination of apps that will work with your particular device.

####Debugging
By default, the installer will generate Debug Logs - _**open\_gapps\_debug\_logs.tar.gz**_ - a compressed file that contains a set of files to help the devs troubleshoot any problems you might experience with the install. This file can be easily attached to any bugreport on GitHub or post on XDA, making it easy for you to provide the devs important information to help troubleshoot any issues you're having. You will find _open\_gapps\_debug\_logs.tar.gz_ in the same folder as your _open\_gapps\_log.txt_. You may disable this feature by adding the keyword `NoDebug` to your gapps-config.
***
Configuring your installation
---
####Presets
You can use Presets with any GApps package. This allows you to transform any GApps package into one of its 'little brothers' by adding one of the following keywords to your gapps-config. This will transform ALL INSTALLER BEHAVIOR (including default removals AND applications available for install) - effectively turning it into a new GApps package.
Valid keyword options are:
  * `StockGApps` - To downsize the following package to Stock GApps. [Super]
  * `FullGApps` - To downsize the following package to Full Modular GApps. [Super/Stock]
  * `MiniGApps` - To downsize any of the following packages to Mini Modular GApps. [Super/Stock/Full]
  * `MicroGApps` - To downsize any of the following packages to Micro Modular GApps. [Super/Stock/Full/Mini]
  * `NanoGApps` - To downsize any of the following packages to Nano Modular GApps. [Super/Stock/Full/Mini/Micro]
  * `PicoGApps` - To downsize any of the following packages to Pico Modular GApps. [Super/Stock/Full/Mini/Micro/Nano]

_**NOTE**: ALL BEHAVIOR OF THE INSTALLER WILL BE TRANSFORMED TO THE NEW PRESET, including default removals AND applications available for install._

####Include and Exclude Google Applications
You can choose either the apps you WANT installed (called an Include Install) or the apps you DON'T WANT installed (default behavior - called an Exclude Install). To select ONLY the apps you WANT installed, add the keyword **Include** to your gapps-config file. The installer will now install ONLY THOSE APPS you have listed in your gapps-config. (Since the default behavior is an Exclude install, it is not necessary to add Exclude to your gapps-config). Stock removals (see below) function the same whether you're doing an Include or Exclude Install.<br>
Type the application keyword (name) you want to Exclude/Include inside your gapps-config file.
Valid keyword options are:
* `AndroidPay` - To Exclude/Include [Android Pay](https://play.google.com/store/apps/details?id=com.google.android.apps.walletnfcrel) [Super]
* `Books` - To Exclude/Include [Google Play Books](https://play.google.com/store/apps/details?id=com.google.android.apps.books) [Super/Stock/Full]
* `CalendarGoogle` - To Exclude/Include [Google Calendar](https://play.google.com/store/apps/details?id=com.google.android.calendar) [Super/Stock/Full/Mini/Micro]
* `CalSync` - To Exclude/Include Google Calendar Sync _(installed ONLY when Google Calendar is NOT being installed)_ [Super/Stock/Full/Mini/Micro/Nano/Pico]
* `CalculatorGoogle` - To Exclude/Include [Google Calculator](https://play.google.com/store/apps/details?id=com.google.android.calculator) [Super/Stock/Full/Mini]
* `CameraGoogle` - To Exclude/Include [Google Camera](https://play.google.com/store/apps/details?id=com.google.android.GoogleCamera) [Super/Stock]
* `Chrome` - To Exclude/Include [Google Chrome Browser](https://play.google.com/store/apps/details?id=com.android.chrome) [Super/Stock/Full]
* `ClockGoogle` - To Exclude/Include [Google Clock](https://play.google.com/store/apps/details?id=com.google.android.deskclock) [Super/Stock/Full/Mini]
* `CloudPrint` - To Exclude/Include [Google Cloud Print](https://play.google.com/store/apps/details?id=com.google.android.apps.cloudprint) [Super/Stock/Full]
* `ContactsGoogle` - To Exclude/Include [Google Contacts](https://play.google.com/store/apps/details?id=com.google.android.contacts) [Super/Stock]
* `DialerFramework` - To Exclude/Include Dialer Framework [Super/Stock/Full/Mini/Micro/Nano/Pico]
* `DialerGoogle` - To Exclude/Include [Google Dialer](https://play.google.com/store/apps/details?id=com.google.android.dialer) [Super/Stock]
* `DMAgent` - To Exclude/Include [Google Apps Device Policy](https://play.google.com/store/apps/details?id=com.google.android.apps.enterprise.dmagent) [Super]
* `Docs` - To Exclude/Include [Google Docs](https://play.google.com/store/apps/details?id=com.google.android.apps.docs.editors.docs) [Super/Stock/Full]
* `Drive` - To Exclude/Include [Google Drive](https://play.google.com/store/apps/details?id=com.google.android.apps.docs) [Super/Stock/Full]
* `Earth` - To Exclude/Include [Google Earth](https://play.google.com/store/apps/details?id=com.google.earth) [Super]
* `ExchangeGoogle` - To Exclude/Include Google Exchange Services [Super/Stock/Full/Mini/Micro]
* `FaceDetect` - To Exclude/Include FaceUnlock [Super/Stock/Full/Mini/Micro/Nano]
* `FaceUnlock` - To Exclude/Include FaceUnlock [Super/Stock/Full/Mini/Micro/Nano]
* `Fitness` - To Exclude/Include [Google Fit](https://play.google.com/store/apps/details?id=com.google.android.apps.fitness) [Super/Stock/Full]
* `GCS` - To Exclude BOTH [Google Connectivity Services](https://play.google.com/store/apps/details?id=com.google.android.apps.gcs) AND [Project Fi by Google](https://play.google.com/store/apps/details?id=com.google.android.apps.tycho) [Super]
**OR** To Include [Google Connectivity Services](https://play.google.com/store/apps/details?id=com.google.android.apps.gcs) [Super]
* `Gmail` - To Exclude/Include [Gmail](https://play.google.com/store/apps/details?id=com.google.android.gm) [Super/Stock/Full/Mini/Micro]
* `GoogleNow` - To Exclude/Include [Google Now Launcher](https://play.google.com/store/apps/details?id=com.google.android.launcher) [Super/Stock/Full/Mini/Micro]
* `GooglePlus` - To Exclude/Include [Google+](https://play.google.com/store/apps/details?id=com.google.android.apps.plus) [Super/Stock/Full/Mini]
* `GoogleTTS` - To Exclude/Include [Google Text-to-Speech](https://play.google.com/store/apps/details?id=com.google.android.tts) [Super/Stock/Full/Mini/Micro (6.0 also Nano/Pico)]
* `Hangouts` - To Exclude/Include [Hangouts](https://play.google.com/store/apps/details?id=com.google.android.talk) [Super/Stock/Full/Mini]
* `Hotword` - To Exclude/Include OK Google Hotword Enrollment [Super/Stock/Full/Mini/Micro/Nano]
* `Indic` - To Exclude/Include [Google Indic Keyboard](https://play.google.com/store/apps/details?id=com.google.android.apps.inputmethod.hindi) [Super]
* `Japanese` - To Exclude/Include [Google Japanese Input](https://play.google.com/store/apps/details?id=com.google.android.inputmethod.japanese) [Super]
* `Keep` - To Exclude/Include [Google Keep](https://play.google.com/store/apps/details?id=com.google.android.keep) [Super/Stock/Full]
* `KeyboardGoogle` - To Exclude/Include [Google Keyboard](https://play.google.com/store/apps/details?id=com.google.android.inputmethod.latin) [Super/Stock]
* `Korean` - To Exclude/Include [Google Korean Input](https://play.google.com/store/apps/details?id=com.google.android.inputmethod.korean) [Super]
* `Maps` - To Exclude/Include [Google Maps](https://play.google.com/store/apps/details?id=com.google.android.apps.maps) [Super/Stock/Full/Mini]
* `Messenger` - To Exclude/Include [Google Messenger](https://play.google.com/store/apps/details?id=com.google.android.apps.messaging) _(not installed on tablet devices)_ [Super/Stock]
* `Movies` - To Exclude/Include [Google Play Movies & TV](https://play.google.com/store/apps/details?id=com.google.android.videos) [Super/Stock/Full]
* `Music` - To Exclude/Include [Google Play Music](https://play.google.com/store/apps/details?id=com.google.android.music) [Super/Stock/Full]
* `NewsStand` - To Exclude/Include [Google Play Newsstand](https://play.google.com/store/apps/details?id=com.google.android.apps.magazines) [Super/Stock/Full]
* `NewsWidget` - To Exclude/Include [Google News & Weather](https://play.google.com/store/apps/details?id=com.google.android.apps.genie.geniewidget) [Super/Stock/Full]
* `PackageInstallerGoogle` - To Exclude/Include Google Package Installer [Super/Stock/Full/Mini/Micro/Nano/Pico]
* `Pinyin` - To Exclude/Include [Google Pinyin Input](https://play.google.com/store/apps/details?id=com.google.android.inputmethod.pinyin) [Super]
* `Photos` - To Exclude/Include [Google Photos](https://play.google.com/store/apps/details?id=com.google.android.apps.photos) [Super/Stock/Full/Mini]
* `PlayGames` - To Exclude/Include [Google Play Games](https://play.google.com/store/apps/details?id=com.google.android.play.games) [Super/Stock/Full]
* `PrintServiceGoogle` - To Exclude/Include Print Service Recommendation Service [Super/Stock]
* `ProjectFi` - To Exclude/Include [Project Fi by Google](https://play.google.com/store/apps/details?id=com.google.android.apps.tycho) [Super]
* `Sheets` - To Exclude/Include [Google Sheets](https://play.google.com/store/apps/details?id=com.google.android.apps.docs.editors.sheets) [Super/Stock/Full]
* `Slides` - To Exclude/Include [Google Slides](https://play.google.com/store/apps/details?id=com.google.android.apps.docs.editors.slides) [Super/Stock/Full]
* `Search` - To Exclude BOTH [Google Search](https://play.google.com/store/apps/details?id=com.google.android.googlequicksearchbox) AND [Google Now Launcher](https://play.google.com/store/apps/details?id=com.google.android.launcher) [Super/Stock/Full/Mini/Micro/Nano]
**OR** To Include [Google Search](https://play.google.com/store/apps/details?id=com.google.android.googlequicksearchbox) AND OK Google Hotword Enrollment [Super/Stock/Full/Mini/Micro/Nano]
* `Speech` - To Exclude/Include off-line Speech files _(For Voice Dictation Offline)_ [Super/Stock/Full/Mini/Micro/Nano]
* `Street` - To Exclude/Include [Google Street View](https://play.google.com/store/apps/details?id=com.google.android.street) [Super]
* `TagGoogle` - To Exclude/Include Google NFC Tags [Super/Stock/Full/Mini]
* `Talkback` - To Exclude/Include [Google TalkBack](https://play.google.com/store/apps/details?id=com.google.android.marvin.talkback) [Super/Stock/Full]
* `Translate` - To Exclude/Include [Google Translate](https://play.google.com/store/apps/details?id=com.google.android.apps.translate) [Super]
* `VRService` - To Exclude/Include Google VR Services [Super/Stock]
* `WebViewGoogle` - To Exclude/Include [Google Webview](https://play.google.com/store/apps/details?id=com.google.android.webview) [Super/Stock]
* `WebViewStub` - To Exclude/Include [Google Webview Stub](https://play.google.com/store/apps/details?id=com.google.android.webview) [Super/Stock] _(Placeholder for Google WebView, on 7.0+ automatically used instead of `WebViewGoogle` if `Chrome` is installed)_ 
* `YouTube` - To Exclude/Include [YouTube](https://play.google.com/store/apps/details?id=com.google.android.youtube) [Super/Stock/Full/Mini]
* `Zhuyin` - To Exclude/Include [Google Zhuyin Input](https://play.google.com/store/apps/details?id=com.google.android.apps.inputmethod.zhuyin) [Super]

####Removal of Stock applications
To manage the removal of certain Stock applications type the application keyword (name) inside your gapps-config file.

_**Stock**_ below means apps from AOSP or built-in to the device. Some manufacturers use different names so we have to add support for them:
* BLU
* CyanogenMod
* Flux
* FlymeOS (BrowserIntl, Browser, CustomizeCenter, EasyLauncher, FileManager, FlymeLauncherIntl, FlymeLauncher, MzMPay, MzPay, MzInput, MzSetupWizard, MzUpdate, SystemUpdate, SystemUpdateAssistant, Weather)
* Lenovo (packageinstaller)
* Miui
* MoKee (Nox launcher, YuBrowser)
* Motorola
* Omni (Apollo, Omni Deskclock2, OmniSwitch)
* Paranoid Android

Valid keyword options are:
* `BasicDreams`- To remove the Basic Dreams Wallpaper
* `Browser` - To remove the Stock Browser
* `CalculatorStock` - To remove the Stock Calculator _(automatically removed when Google Calculator is installed)_
* `CalendarStock` - To remove the Stock Calendar _(automatically removed when Google Calendar is installed)_
* `CameraStock` - To remove the Stock Camera
* `ClockStock` - To remove the Stock Desk Clock _(automatically removed when Google Desk Clock is installed)_
* `CMAccount` - To remove the CM Account Application
* `CMAudioFX` - To remove CM AudioFX
* `CMFileManager` - To remove CM File Manager
* `CMMusic` - To remove CM Music
* `CMScreenCast` - To remove the CM ScreenCast app
* `CMSetupWizard` - To remove the CM Setup Wizard _(see [[Notes for CMSetupWizard]])_
* `CMUpdater` - To remove CM Updater
* `CMWallpapers` - To remove the CM Wallpapers
* `CMWeatherProvider` - To remove the CM Weather Underground
* `DashClock` - To remove DashClock Widget _(found in certain ROMs)_
* `Email` - To remove the Stock Email Client
* `ExchangeStock` - To remove Stock Exchange Services _(automatically removed when Google Exchange Services is installed)_
* `FMRadio` - To remove the Stock FM Radio _(not found on all devices or ROMs)_
* `Gallery` - To remove the Stock Gallery
* `Galaxy` - To remove the Galaxy (also known as BlackHole) Wallpaper
* `Hexo` - To remove the Hexo Libre Theme
* `HoloSpiral` - To remove the Holo Spiral Wallpaper
* `KeyboardStock` - To remove the Stock Keyboard _(automatically removed when Google Keyboard is installed)_
* `Launcher` - To remove the Stock Launcher(s)
* `LiveWallpapers` - To remove the Stock Live Wallpapers
* `LockClock` -  To remove the Stock Lockscreen Clock Widget
* `MMS` - To remove the Stock SMS _(automatically removed if Google Messenger and/or Hangouts is installed)_
* `MzFileManager` - To remove the Stock FlymeOS File Manager
* `MzPay` - To remove the Stock FlymeOS Pay system _(because MzPay services works only in China)_
* `MzSetupWizard` - To remove the Stock FlymeOS SetupWizard
* `MzUpdater` - To remove the Stock FlymeOS Updaters
* `MzWeather` - To remove the Stock FlymeOS Weather _(because MzWeather service work only in China)_
* `NoiseField` - To remove the Noise Field Wallpaper
* `OmniSwitch` - To remove the OmniSwitch recent apps switcher replacement
* `Phasebeam` - To remove the Phasebeam Wallpaper
* `PhotoPhase` - To remove the Photo Phase Wallpaper
* `PhotoTable` - To remove the Photo Table Wallpaper
* `PicoTTS` - To remove the Stock PicoTTS
* `PrintServiceStock` - To remove the Stock Print Service Recommendation Service _(automatically removed when Google Print Service Recommendation Service is installed)_
* `SimToolKit` - To remove the Stock SimToolKit
* `Studio` - To remove the Stock Movie Studio
* `SykoPath` - To remove SykoPath Layers Manager _(found in certain ROMs)_
* `TagStock` - To remove the Stock NFC Tags _(automatically removed when Google NFC Tags is installed)_
* `Terminal` - To remove the Stock Terminal
* `Themes` - To remove the Stock Theme Engine _(Will break the Settings Entry and can cause unexpected reboots on some ROMs)_
* `VisualizationWallpapers` - To remove the Stock Visualization Wallpapers
* `WhisperPush`- To remove the Stock WhisperPush support
<br><br>To prevent the default removal of the Stock apps (listed below) when using the Open GApps Super/Stock package, type the keyword option preceded by a '+' as shown below:
  * `+Browser` - To bypass the automatic removal of Stock Browser [Super/Stock]
  * `+CameraStock` - To bypass the automatic removal of Stock Camera [Super/Stock]
  * `+Email` - To bypass the automatic removal of Stock Email [Super/Stock]
  * `+Gallery` - To bypass the automatic removal of Stock Gallery [Super/Stock]
  * `+Launcher` - To bypass the automatic removal of Stock Launcher(s) [Super/Stock]
  * `+MMS` - To bypass the automatic removal of Stock SMS [Super/Stock]
  * `+PicoTTS` - To bypass the automatic removal of the Stock PicoTTS app [Super/Stock]

_**NOTE**: The installer will automatically NOT remove the Stock application if its Google counterpart is NOT being installed. For example, if you are NOT installing Hangouts or Messenger, then the Stock MMS app will NOT automatically be removed (although you can still force its removal by adding it to your gapps-config). The same is true for Google Camera|Stock Camera, Gmail|Stock Email, Google Exchange Services|Stock Exchange Services, Google Keyboard|Stock Keyboard, Photos|Stock Gallery, Google Now Launcher|Stock Launcher, GoogleTTS|PicoTTS, Google WebView(or Stub)|Stock WebView and Google Calendar|Stock Calendar.

####Universal Application Removals
In addition to the Stock Removals above, Universal Application Removals is available in the Open GApps installer. Universal Removals allow you to remove ANY system app on your device or ROM, with the EXCEPTION of (core) apps that are part of Open GApps itself.
To use this feature, enclose the name of the apk in parentheses inside your gapps-config file.
See below for complete details:

For example to remove the Spare Parts app found in many ROMs, simply add `(SpareParts)` to your gapps-config. When using this feature, keep the following in mind:
* Adding the .apk extension is not required (however, it will work)
* Works for all apps in any system/app or system/priv-app subfolder
* Removes the entire contents of the folder containing the apk (including subfolders)
* Removal is also added to the addon.d backup script so the removals will also be applied if you update your ROM
* Gives you the ability to do some really bad things to your device, so **DO A BACKUP** before trying

_**WARNING**: Because this feature gives you the ability to remove files that may be important to the proper function of your device, it is only recommended for very experienced users who know what they are doing._

####Force DPI Setting
Open GApps normally selects the correct DPI-optimized app that suits your device, based on the information that is supplied by recovery and otherwise found in default.prop or build.prop. Sometimes one might want to override this DPI setting, e.g. for testing, in those situations the keyword `forcedpiXXX` can be used, where XXX is replaced with one of the [valid default DPIs](http://developer.android.com/reference/android/util/DisplayMetrics.html) including: 160, 240, 320, 480, 560 or 640.
####Force New Camera
Open GApps normally detects if the device is deemed compatible with the _New Camera API_ based on fields specified in `build.prop` and a whitelist. If not deemed compatible, the newest Google Camera (version 3 and higher) will not be installed but the older version 2 instead (`googlecameralegacy`). To override this detection the `forcenewcamera` keyword can be used. Note: Google Camera version 3 does not work correctly on most non-Nexus devices.
####Skip Google's Swype Library Setting		
The Stock keyboard does normally not support gesture typing. If Google Keyboard is not being installed, Open GApps installs by default Google's swype gesture libraries to the Stock keyboard. The libraries are installed in addition to the AOSP libraries. In some cases adding these libraries is unwanted behavior (there are few reports that recent these can conflict with certain ROMs). In those situations use the `skipswypelibs` keyword to skip the installation of these libraries (or remove them if previously installed).
####Substitute AOSP Library with Google's Swype Library Setting		
The Stock keyboard does normally not support gesture typing. If Google Keyboard is not being installed, Open GApps installs by default Google's swype gesture libraries to the Stock keyboard. The libraries are installed in addition to the AOSP libraries. In some cases these gesture libraries only work if they are installed as a _replacement_ of the AOSP libraries (there are few reports that this is necessary with certain ROMs). In those situations use the `substituteswypelibs` keyword to replace the Stock libraries. (If you re-run the installation without the keyword, the AOSP libraries are restored to their original configuration).
####Skip updating vendor libraries
Open GApps by default updates certain libraries that are depended on by certain GApps (especially Face Unlock) that are stored in `/system/vendor` (or a `/vendor` partition via a symlink). To prevent GApps from touching (removing, adding or replacing) these vendor files use the `skipvendorlibs` keyword.
####Skip Smart Pre-ODEXing of APKs
On Marshmallow some ROMs are set to be extremely strict when verifying the APK. This can lead to de-odexed APKs to fail verification; because the included classes.dex is not present in the APK's MANIFEST. To avoid this potential issue, Open GApps by default pre-ODEXes these APKs on 6.0+. As positive side-effect this setting also improves the performance of these applications. A downside is that it occupies more disk-space on /system, because a copy of the classes.dex has to be kept for regenerating the ODEX when updating the ROM. To disable this feature use the keyword `NoPreODEX`. **THE PRE-ODEX FEATURE IS TEMPORARILY DISABLED BY DEFAULT; SEE BELOW HOW TO ENABLE**
####Enable Smart Pre-ODEXing of APKs
To enable Pre-ODEXing on ROMs the `PreODEX` can be used.
####Force Clean Install Setting
Open GApps normally detects if it's a clean install or an upgrade. This affects how installation of Google Camera is treated, it won't install those unless this is a clean install to avoid problems during upgrades. To ignore the detection and enforce clean install use `forceclean` keyword. Note: this setting is untested widely and may cause problems.
***
Miscellaneous
---
* You can add notes or comments to your gapps-config using a `#`. Anything following a `#` will be ignored until the end of that line.
For example:
  * `# Exclude Search` would be completely ignored
  * While `Search # Exclude Search` would process the first `Search` keyword (since it appeared BEFORE the '#')

* _"Protection from Stupidity"_ is built into the GApps Installer. To prevent you from accidentally leaving yourself with no keyboard, Launcher, or MMS app when you start your device, the installer WILL NOT ALLOW you to remove the Stock Keyboard, Launcher, or MMS app if you are not also installing a Google version of these apps. You can, however, override this protection by adding the keyword `Override` to your gapps-config. Be very careful when using this option and make certain you have a replacement app already installed on your device before using this option. This keyword can also be used to override the automatic selection of `WebViewStub` over `WebViewGoogle` if `Chrome` is being installed.

* Case, order, spaces, or using empty lines does not matter when using gapps-config.