Advanced Features and Options
===
The features outlined below are COMPLETELY OPTIONAL and designed to allow advanced users the ability to modify the default behavior of the Open GApps installers. Without the use of these options, the installers will function exactly as described in [[Package Comparison|Package-Comparison]] chart.

The gapps-config file
---
To modify the default behavior of the Open GApps installer, create a text file called **.gapps-config** or **gapps-config.txt** (.gapps-config will take precedence) and place it in the **same folder as the Open GApps zip** or in **/sdcard/Open-GApps** (zip folder will take precedence). Once you've created the gapps-config file, simply type in the keyword options you want from the lists below. There is also a more user-friendly front-end available that can generate the gapps-config file for you behind the scenes: the [AROMA Open GApps installer](http://forum.xda-developers.com/android/general/open-gapps-aroma-installer-t3010798). 

####Testing
To perform a test installation that will only simulate an install, add the keyword `Test` to your gapps-config. The installer will perform all system space calculations and generate a detailed log _**open\_gapps\_log.txt** _(in the same folder as your gapps-config), but WILL NOT MAKE ANY CHANGES to your device. This should be helpful for trying to find just the right combination of apps that will work with your particular device.

####Debugging
By default, the installer will generate Debug Logs - _**open_gapps_debug_logs.tar.gz**_ - a compressed file that contains a set of files to help the devs troubleshoot any problems you might experience with the install. This file can be easily attached to any bugreport on GitHub or post on XDA, making it easy for you to provide the devs important information to help troubleshoot any issues you're having. You will find _open\_gapps\_debug\_logs.tar.gz_ in the same folder as your _open\_gapps\_log.txt_. You may disable this feature by adding the keyword `NoDebug` to your gapps-config.
***
Configuring your installation
---
####Presets
You can use Presets with any GApps package. This allows you to transform any GApps package into one of its 'little brothers' by adding one of the following keywords to your gapps-config. This will transform ALL INSTALLER BEHAVIOR (including default removals AND applications available for install) - effectively turning it into a new GApps package.
Valid keyword options are:
  * `FullGApps` - To downsize the following package to Full Modular GApps. [Stock]
  * `MiniGApps` - To downsize any of the following packages to Mini Modular GApps. [Stock/Full]
  * `MicroGApps` - To downsize any of the following packages to Micro Modular GApps. [Stock/Full/Mini]
  * `NanoGApps` - To downsize any of the following packages to Nano Modular GApps. [Stock/Full/Mini/Micro]
  * `PicoGApps` - To downsize any of the following packages to Pico Modular GApps. [Stock/Full/Mini/Micro/Nano]

_**NOTE**: ALL BEHAVIOR OF THE INSTALLER WILL BE TRANSFORMED TO THE NEW PRESET, including default removals AND applications available for install._

####Include and Exclude Google Applications
You can choose either the apps you WANT installed (called an Include Install) or the apps you DON'T WANT installed (default behavior - called an Exclude Install). To select ONLY the apps you WANT installed, add the keyword **Include** to your gapps-config file. The installer will now install ONLY THOSE APPS you have listed in your gapps-config. (Since the default behavior is an Exclude install, it is not necessary to add Exclude to your gapps-config). Stock/AOSP removals (see below) function the same whether you're doing an Include or Exclude Install.<br>
Type the application keyword (name) you want to Exclude/Include inside your gapps-config file.
Valid keyword options are:
* `Books` - To Exclude/Include Google Play Books [Stock/Full]
* `CalendarGoogle` - To Exclude/Include Google Calendar [Stock/Full/Mini/Micro]
* `CalSync` - To Exclude/Include Google Calendar Sync _(installed by default when Google Calendar is NOT being installed)_ [Stock/Full/Mini/Micro/Nano/Pico]
* `CameraGoogle` - To Exclude/Include Google Camera [Stock]
* `Chrome` - To Exclude/Include Chrome Browser [Stock/Full]
* `CloudPrint` - To Exclude/Include Cloud Print [Stock/Full]
* `Docs` - To Exclude/Include Google Docs [Stock/Full]
* `Drive` - To Exclude/Include Google Drive [Stock/Full]
* `Ears` - To Exclude/Include Sound Search for Google Play [Stock/Full]
* `Earth` - To Exclude/Include Google Earth [Stock/Full]
* `ExchangeGoogle` - To Exclude/Include Google Exchange Services [Stock/Full/Mini/Micro]
* `FaceUnlock` - To Exclude/Include FaceUnlock [Stock/Full/Mini/Micro]
* `Fitness` - To Exclude/Include Google Fit [Stock/Full]
* `Gmail` - To Exclude/Include Gmail [Stock/Full/Mini/Micro]
* `GoogleNow` - To Exclude/Include Google Now Launcher [Stock/Full/Mini/Micro]
* `GooglePlus` - To Exclude/Include Google+ [Stock/Full/Mini]
* `GoogleTTS` - To Exclude/Include Google Text-to-Speech [Stock/Full/Mini/Micro]
* `Hangouts` - To Exclude/Include Hangouts [Stock/Full/Mini]
* `Keep` - To Exclude/Include Google Keep [Stock/Full]
* `KeyboardGoogle` - To Exclude/Include Google Keyboard [Stock]
* `Maps` - To Exclude/Include Maps [Stock/Full/Mini]
* `Messenger` - To Exclude/Include Messenger _(not installed on tablet devices)_ [Stock/Full]
* `Movies` - To Exclude/Include Google Play Movies & TV [Stock/Full]
* `Music` - To Exclude/Include Google Play Music [Stock/Full]
* `NewsStand` - To Exclude/Include Google Play Newsstand [Stock/Full]
* `NewsWidget` - To Exclude/Include Google News & Weather [Stock/Full]
* `Photos` - To Exclude/Include Photos [Stock/Full/Mini]
* `PlayGames` - To Exclude/Include Google Play Games [Stock/Full]
* `Sheets` - To Exclude/Include Google Sheets [Stock/Full]
* `Slides` - To Exclude/Include Google Slides [Stock/Full]
* `Search` - To Exclude BOTH Google Search AND Google Now Launcher [Stock/Full/Mini/Micro/Nano]
**OR** To Include Google Search [Stock/Full/Mini/Micro/Nano]
* `Speech` - To Exclude/Include off-line Speech files _(Required for off-line "Okay Google" support)_ [Stock/Full/Mini/Micro/Nano]
* `Street` - To Exclude/Include Street View on Google Maps [Stock/Full/Mini]
* `Talkback` - To Exclude/Include TalkBack [Stock/Full]
* `Wallet` - To Exclude/Include Google Wallet [Stock/Full]
* `Webview` - To Exclude/Include Google Webview [Stock/Full]
* `YouTube` - To Exclude/Include YouTube [Stock/Full/Mini]

####Removal of Stock applications
To manage the removal of certain Stock/AOSP applications type the application keyword (name) inside your gapps-config file.
Valid keyword options are:
* `BasicDreams`- To remove the Stock Basic Dreams Wallpaper
* `Browser` - To remove the Stock/AOSP Browser
* `CalendarStock` - To remove the Stock/AOSP Calendar Application _(automatically removed when Google Calendar is installed)_
* `CameraStock` - To remove the Stock/AOSP Camera Application _(automatically removed when Google Camera is installed)_
* `CMAccount` - TO remove the Stock CM Account Application
* `CMAudioFX` - To remove the Stock CM AudioFX Application
* `CMEleven` - To remove the Stock CM Music Application
* `CMFileManager` - To remove the Stock CM File Manager Application
* `CMUpdater` - To remove the Stock CM Updater Application
* `CMSetupWizard` - To remove the Stock CM Setup Wizard Application
* `CMWallpapers` - To remove the Stock CM Wallpapers
* `DashClock` - To remove the Stock DashClock Application _(found in certain ROM's)_
* `Email` - To remove the Stock/AOSP Email Application
* `ExchangeStock` - To remove the Stock/AOSP Exchange Services _(automatically removed when Google Exchange Services is installed)_
* `FMRadio` - To remove the Stock FM Radio Application _(not found on all devices or ROM's)_
* `Gallery` - To remove the Stock/AOSP Gallery Application
* `Galaxy` - To remove the Stock Galaxy Wallpaper
* `HoloSpiral` - To remove the Stock Holo Spiral Wallpaper
* `KeyboardStock` - To remove the Stock/AOSP Keyboard _(automatically removed when Google Keyboard is installed)_
* `Launcher` - To remove the Stock/AOSP Launcher(s)
* `LiveWallpapers` - To remove the Stock Live Wallpapers
* `LockClock` -  To remove the Stock Lock Clock Application
* `MMS` - To remove the Stock/AOSP SMS Application
* `NoiseField` - To remove the Stock Noise Field Wallpaper
* `Phasebeam` - To remove the Stock Phasebeam Wallpaper
* `PhotoPhase` - To remove the Stock Photo Phase Wallpaper
* `PhotoTable` - To remove the Stock Photo Table Wallpaper
* `PicoTTS` - To remove the Stock/AOSP PicoTTS
* `SimToolKit` - To remove the Stock/AOSP SimToolKit Application
* `Studio` - To remove the Stock/AOSP Movie Studio Application
* `SykoPath` - To remove SykoPath OverlayManager _(found in certain ROM's)_
* `Terminal` - To remove the Stock Terminal Application
* `Themes` - To remove the Stock Themes Application _(Will break the link in Settings to Themes)_
* `VisualizationWallpapers` - To remove the Stock Visualization Wallpapers
* `WhisperPush`- To remove the Stock WhisperPush support
<br><br>The information below pertains ONLY to Google Stock GApps packages.<br>
To bypass the default removal of the Stock/AOSP apps (listed below) when using Google Stock GApps, type the keyword option preceded by a '+' as shown below:
  * `+Browser` - To bypass the automatic removal of Stock/AOSP Browser [Stock ONLY]
  * `+Email` - To bypass the automatic removal of Stock/AOSP Email Application [Stock ONLY]
  * `+Gallery` - To bypass the automatic removal of Stock/AOSP Gallery Application [Stock ONLY]
  * `+Launcher` - To bypass the automatic removal of Stock/AOSP Launcher(s) [Stock ONLY]
  * `+MMS` - To bypass the automatic removal of Stock/AOSP SMS Application [Stock ONLY]
  * `+PicoTTS` - To bypass the automatic removal of the Stock/AOSP PicoTTS app [Stock ONLY]
  * `+WebViewStock` - To bypass the automatic removal of the Stock/AOSP WebView library [Stock ONLY]

_**NOTE**: The installer will automatically NOT remove the Stock/AOSP application if its Google counterpart is NOT being installed. For example, if you are NOT installing Hangouts or Messenger, then the Stock MMS app will NOT automatically be removed (although you can still force its removal by adding it to your gapps-config). The same is true for Google Camera|Stock Camera, Gmail|Stock Email, Google Exchange Services|Stock Exchange Services, Google Keyboard|Stock Keyboard, Photos|Stock Gallery, Google Now Launcher|Stock Launcher, GoogleTTS|PicoTTS, and Google Calendar|Stock Calendar._
***
Miscellaneous
---
* You can add notes or comments to your gapps-config using a `#`. Anything following a `#` will be ignored until the end of that line.
For example:
  * `# Exclude Search` would be completely ignored
  * While `Search # Exclude Search` would process the first `Search` keyword (since it appeared BEFORE the '#')

* _"Protection from Stupidity"_ is built into the GApps Installer. To prevent you from accidentally leaving yourself with no keyboard, Launcher, or MMS app when you start your device, the installer WILL NOT ALLOW you to remove the Stock/AOSP Keyboard, Launcher, or MMS app if you are not also installing a Google version of these apps. You can, however, override this protection by adding the keyword `Override` to your gapps-config. Be very careful when using this option and make certain you have a replacement app already installed on your device before using this option.

* Case, order, spaces, or using separate lines does not matter when using gapps-config.