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
You can choose either the apps you WANT installed (called an Include Install) or the apps you DON'T WANT installed (default behavior - called an Exclude Install). To select ONLY the apps you WANT installed, add the keyword **Include** to your gapps-config file. The installer will now install ONLY THOSE APPS you have listed in your gapps-config. (Since the default behavior is an Exclude install, it is not necessary to add Exclude to your gapps-config). Stock/AOSP removals (see below) function the same whether you're doing an Include or Exclude Install.<br>
Type the application keyword (name) you want to Exclude/Include inside your gapps-config file.
Valid keyword options are:
* `AndroidPay` - To Exclude/Include Android Pay [Super]
* `AndroidForWork` - To Exclude/Include Android For Work [Super]
* `Books` - To Exclude/Include Google Play Books [Super/Stock/Full]
* `CalendarGoogle` - To Exclude/Include Google Calendar [Super/Stock/Full/Mini/Micro]
* `CalSync` - To Exclude/Include Google Calendar Sync _(installed by default when Google Calendar is NOT being installed)_ [Super/Stock/Full/Mini/Micro/Nano/Pico]
* `CalculatorGoogle` - To Exclude/Include Google Calculator [Super/Stock/Full/Mini]
* `CameraGoogle` - To Exclude/Include Google Camera [Super/Stock]
* `Chrome` - To Exclude/Include Chrome Browser [Super/Stock/Full]
* `ClockGoogle` - To Exclude/Include Google Desk Clock [Super/Stock/Full/Mini]
* `CloudPrint` - To Exclude/Include Cloud Print [Super/Stock/Full]
* `ContactsGoogle` - To Exclude/Include Google Contacts [Super/Stock]
* ~~`DialerGoogle` - To Exclude/Include Google Dialer [Super/Stock]~~ 
* `DMAgent` - To Exclude/Include Google Apps Device Policy [Super]
* `Docs` - To Exclude/Include Google Docs [Super/Stock/Full]
* `Drive` - To Exclude/Include Google Drive [Super/Stock/Full]
* `Ears` - To Exclude/Include Sound Search for Google Play [Super/Stock/Full]
* `Earth` - To Exclude/Include Google Earth [Super]
* `ExchangeGoogle` - To Exclude/Include Google Exchange Services [Super/Stock/Full/Mini/Micro]
* `FaceDetect` - To Exclude/Include FaceUnlock [Super/Stock/Full/Mini/Micro/Nano]
* `FaceUnlock` - To Exclude/Include FaceUnlock [Super/Stock/Full/Mini/Micro/Nano]
* `Fitness` - To Exclude/Include Google Fit [Super/Stock/Full]
* `GCS` - To Exclude BOTH Google Connectivity Services AND Project Fi by Google [Super]
**OR** To Include Google Connectivity Services [Super]
* `Gmail` - To Exclude/Include Gmail [Super/Stock/Full/Mini/Micro]
* `GoogleNow` - To Exclude/Include Google Now Launcher [Super/Stock/Full/Mini/Micro]
* `GooglePlus` - To Exclude/Include Google+ [Super/Stock/Full/Mini]
* `GoogleTTS` - To Exclude/Include Google Text-to-Speech [Super/Stock/Full/Mini/Micro]
* `Hangouts` - To Exclude/Include Hangouts [Super/Stock/Full/Mini]
* `Indic` - To Exclude/Include Google Indic Keyboard [Super]
* `Japanese` - To Exclude/Include Google Japanese Input [Super]
* `Keep` - To Exclude/Include Google Keep [Super/Stock/Full]
* `KeyboardGoogle` - To Exclude/Include Google Keyboard [Super/Stock]
* `Korean` - To Exclude/Include Google Korean Input [Super]
* `Maps` - To Exclude/Include Maps [Super/Stock/Full/Mini]
* `Messenger` - To Exclude/Include Messenger _(not installed on tablet devices)_ [Super/Stock]
* `Movies` - To Exclude/Include Google Play Movies & TV [Super/Stock/Full]
* `Music` - To Exclude/Include Google Play Music [Super/Stock/Full]
* `NewsStand` - To Exclude/Include Google Play Newsstand [Super/Stock/Full]
* `NewsWidget` - To Exclude/Include Google News & Weather [Super/Stock/Full]
* `PackageInstallerGoogle` - To Exclude/Include Google Package Installer [Super/Stock/Full/Mini/Micro/Nano/Pico]
* `Pinyin` - To Exclude/Include Google Pinyin Input [Super]
* `Photos` - To Exclude/Include Photos [Super/Stock/Full/Mini]
* `PlayGames` - To Exclude/Include Google Play Games [Super/Stock/Full]
* `ProjectFi` - To Exclude/Include Project Fi by Google [Super]
* `Sheets` - To Exclude/Include Google Sheets [Super/Stock/Full]
* `Slides` - To Exclude/Include Google Slides [Super/Stock/Full]
* `Search` - To Exclude BOTH Google Search AND Google Now Launcher [Super/Stock/Full/Mini/Micro/Nano]
**OR** To Include Google Search [Super/Stock/Full/Mini/Micro/Nano]
* `Speech` - To Exclude/Include off-line Speech files _(Required for off-line "Okay Google" support)_ [Super/Stock/Full/Mini/Micro/Nano]
* `Street` - To Exclude/Include Google Street View [Super]
* `TagGoogle` - To Exclude/Include Google NFC Tags [Super/Stock/Full/Mini]
* `Talkback` - To Exclude/Include TalkBack [Super/Stock/Full]
* `Translate` - To Exclude/Include Google Translate [Super]
* `WebviewGoogle` - To Exclude/Include Google Webview [Super/Stock]
* `YouTube` - To Exclude/Include YouTube [Super/Stock/Full/Mini]
* `Zhuyin` - To Exclude/Include Google Zhuyin Input [Super]

####Removal of Stock applications
To manage the removal of certain Stock/AOSP applications type the application keyword (name) inside your gapps-config file.
Valid keyword options are:
* `BasicDreams`- To remove the Stock Basic Dreams Wallpaper
* `Browser` - To remove the Stock/AOSP/BLU Browser
* `CalendarStock` - To remove the Stock/AOSP/BLU Calendar Application _(automatically removed when Google Calendar is installed)_
* `CameraStock` - To remove the Stock/AOSP/CM(Snap)/Moto/BLU Camera Application
* `ClockStock` - To remove the Stock/AOSP/BLU Desk Clock Application _(automatically removed when Google Desk Clock is installed)_
* `CMAccount` - TO remove the Stock CM Account Application
* `CMAudioFX` - To remove the Stock CM AudioFX Application
* `CMFileManager` - To remove the Stock CM File Manager Application
* `CMMusic` - To remove the Stock CM Music Application
* `CMUpdater` - To remove the Stock CM Updater Application
* `CMSetupWizard` - To remove the Stock CM Setup Wizard Application
* `CMWallpapers` - To remove the Stock CM Wallpapers
* `DashClock` - To remove the Stock DashClock Application _(a widget found in certain ROMs)_
* `Email` - To remove the Stock/AOSP/BLU Email Application _(automatically removed when Gmail is installed)_
* `ExchangeStock` - To remove the Stock/AOSP Exchange Services _(automatically removed when Google Exchange Services is installed)_
* `FMRadio` - To remove the Stock FM Radio Application _(not found on all devices or ROMs)_
* `Gallery` - To remove the Stock/AOSP/Moto/BLU Gallery Application
* `Galaxy` - To remove the Stock Galaxy (also known as BlackHole) Wallpaper
* `HoloSpiral` - To remove the Stock Holo Spiral Wallpaper
* `KeyboardStock` - To remove the Stock/AOSP/BLU Keyboard _(automatically removed when Google Keyboard is installed)_
* `Launcher` - To remove the Stock/AOSP/CM/BLU Launcher(s)
* `LiveWallpapers` - To remove the Stock Live Wallpapers
* `LockClock` -  To remove the Stock Lock Clock Application
* `MMS` - To remove the Stock/AOSP/BLU SMS Application _(automatically removed if Google Messenger and/or Hangouts is installed)_
* `NoiseField` - To remove the Stock Noise Field Wallpaper
* `Phasebeam` - To remove the Stock Phasebeam Wallpaper
* `PhotoPhase` - To remove the Stock Photo Phase Wallpaper
* `PhotoTable` - To remove the Stock Photo Table Wallpaper
* `PicoTTS` - To remove the Stock/AOSP PicoTTS
* `SimToolKit` - To remove the Stock/AOSP SimToolKit Application
* `Studio` - To remove the Stock/AOSP Movie Studio Application
* `SykoPath` - To remove SykoPath OverlayManager _(found in certain ROMs)_
* `TagStock` - To remove the Stock/AOSP NFC Tags Application _(automatically removed when Google NFC Tags is installed)_
* `Terminal` - To remove the Stock Terminal Application
* `Themes` - To remove the Stock Themes Application _(Will break the link in Settings to Themes and can cause unexpected reboots on some ROMs)_
* `VisualizationWallpapers` - To remove the Stock Visualization Wallpapers
* `WhisperPush`- To remove the Stock WhisperPush support
<br><br>To prevent the default removal of the Stock/AOSP apps (listed below) when using the Open GApps stock package, type the keyword option preceded by a '+' as shown below:
  * `+Browser` - To bypass the automatic removal of Stock/AOSP Browser [Super/Stock]
  * `+CameraStock` - To bypass the automatic removal of Stock/AOSP/(Snap)CM/Moto/BLU Camera [Super/Stock]
  * `+Email` - To bypass the automatic removal of Stock/AOSP/BLU Email Application [Super/Stock]
  * `+Gallery` - To bypass the automatic removal of Stock/AOSP/Moto/BLU Gallery Application [Super/Stock]
  * `+Launcher` - To bypass the automatic removal of Stock/AOSP/CM/BLU Launcher(s) [Super/Stock]
  * `+MMS` - To bypass the automatic removal of Stock/AOSP/BLU SMS Application [Super/Stock]
  * `+PicoTTS` - To bypass the automatic removal of the Stock/AOSP PicoTTS app [Super/Stock]

_**NOTE**: The installer will automatically NOT remove the Stock/AOSP application if its Google counterpart is NOT being installed. For example, if you are NOT installing Hangouts or Messenger, then the Stock MMS app will NOT automatically be removed (although you can still force its removal by adding it to your gapps-config). The same is true for Google Camera|Stock Camera|CM Snap Camera|Moto Camera, Gmail|Stock Email, Google Exchange Services|Stock Exchange Services, Google Keyboard|Stock Keyboard, Photos|Stock Gallery|Moto Gallery, Google Now Launcher|Stock Launcher, GoogleTTS|PicoTTS, Google WebView|Stock WebView and Google Calendar|Stock Calendar._

####Universal Application Removals
In addition to the Stock/AOSP Removals above, Universal Application Removals is available in the Open GApps installer. Universal Removals allow you to remove ANY system app on your device or ROM, with the EXCEPTION of (core) apps that are part of Open GApps itself.
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
Open GApps normally selects the correct the DPI-optimized app that suits your device, based on the information that is supplied by recovery and otherwise found in defeault.prop or build.prop. Sometimes one might want to override this DPI setting, e.g. for testing, in those situations the keyword `forcedpiXXX` can be used, where XXX is replaced with one of the [valid default DPIs](http://developer.android.com/reference/android/util/DisplayMetrics.html) including: 160, 240, 320, 480, 560 or 640.
####Skip Google's Swype Library Setting		
The Stock/AOSP keyboard does normally not support gesture typing. Open GApps normally adds Google's swype gesture libraries to the Stock/AOSP keyboard during installation. In some cases this behavior is unwanted (there are few reports that recent these can conflict with certain ROMs). In those situations use the `skipswypelibs` keyword to skip the install of these libraries (or remove them if previously installed).
####Force Clean Install Setting
Open GApps normally detects if it's a clean install or an upgrade. This affects how installation of Google Camera is treated, it won't install those unless this is a clean install to avoid problems during upgrades. To ignore the detection and enforce clean install use `forceclean` keyword. Note: this setting is untested widely and may cause problems.
***
Miscellaneous
---
* You can add notes or comments to your gapps-config using a `#`. Anything following a `#` will be ignored until the end of that line.
For example:
  * `# Exclude Search` would be completely ignored
  * While `Search # Exclude Search` would process the first `Search` keyword (since it appeared BEFORE the '#')

* _"Protection from Stupidity"_ is built into the GApps Installer. To prevent you from accidentally leaving yourself with no keyboard, Launcher, or MMS app when you start your device, the installer WILL NOT ALLOW you to remove the Stock/AOSP Keyboard, Launcher, or MMS app if you are not also installing a Google version of these apps. You can, however, override this protection by adding the keyword `Override` to your gapps-config. Be very careful when using this option and make certain you have a replacement app already installed on your device before using this option.

* Case, order, spaces, or using empty lines does not matter when using gapps-config.