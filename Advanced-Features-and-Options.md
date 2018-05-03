All variants of the Open GApps installer (except Aroma\*) will look for and take extra configuation options from a **gapps-config** file. This file is completely optional; without it, the installers will function exactly as described in the [[Package Comparison|Package-Comparison]] chart.

The gapps-config file allows for these kinds of customizations and more:

- You can limit which GApps are installed.  
  (example use case: "I don't want Google Play Books to be installed.")
- You can limit which stock apps the installer removes.  
  (example use case: "I want to install Google Camera but I don't want the stock camera removed.")
- You can make the installer remove stock apps apps of your choice.  
  (example use case: "I want to remove the stock Spare Parts app.")

\* The [[Aroma Package]] includes the Super package and a GUI that provides roughly the same set of customizations as the gapps-config file. It can load and save configurations, but it uses its own format and will not read the gapps-config file.


## gapps-config file location

The gapps-config file must be named one of the following:

 - `.gapps-config` (takes precedence)
 - `gapps-config.txt`

The gapps-config file must be placed in one of the following folders:

 - the folder containing the Open GApps installer (takes precedence)
 - `/sdcard/Open-GApps`
 - `/persist`
 - `/tmp/install`

You can have a device-specific gapps-config file. You will need your device name, which you can find in `open_gapps_log.txt` or in the name of your ROM download. The gapps-config file must be named one of the following:

 - `.gapps-config-DEVICENAME`
 - `gapps-config-DEVICENAME.txt`

Device-specific config files will take precedence over the non-device-specific ones.


## Writing and testing the gapps-config file

The gapps-config file consists of one keyword per line. The available keywords are categorized in the sections below.


### Comments and whitespace

You can add notes or comments to your gapps-config using a `#`. Anything following a `#` will be ignored until the end of that line. For example, `# Exclude Search` would be completely ignored, while `Search # Exclude Search` would process the first `Search` keyword (since it appeared BEFORE the `#`).

Case, order, spaces, and empty lines are ignored in the gapps-config file.


### Testing

To perform a test installation that will only simulate an install, add the keyword `Test` to your gapps-config. The installer will perform all system space calculations and generate a detailed `open_apps_log.txt` file (in the same folder as your gapps-config), but WILL NOT MAKE ANY CHANGES to your device. This should be helpful for trying to find just the right combination of apps that will work with your particular device.


### Debug logs

By default, the installer will generate Debug Logs that can help the devs troubleshoot any problems you might experience with the install. The logs are compressed and stored in a file named `open_gapps_debug_logs.tar.gz` in the same folder as the `open_apps_log.txt` file. This file can be easily attached to any bugreport on GitHub or post on XDA, making it easy for you to provide the devs important information to help troubleshoot any issues you're having. You may disable this feature by adding the keyword `NoDebug` to your gapps-config.


## Configuring your installation
By default (without a config file), the installation script will first remove all previously installed Google Apps and then install every app that is to be installed from the GApps package . In addition, the installation will remove the stock apps that are replaced by their GApp-counterpart, unless configured not to. There are several options available to alter and extend this behaviour.

### Downsizing

You can transform any GApps package into one of its "little brothers" by adding one of the following keywords to your gapps-config. This will transform ALL INSTALLER BEHAVIOUR (including default removals AND applications available for install) -- effectively turning it into the smaller GApps package. **[TODO: Add here whether or not you can still use other entries in the config file after downsizing] **

Valid keyword options are:

  * `StockGApps` [Super+]
  * `FullGApps` [Stock+]
  * `MiniGApps` [Full+]
  * `MicroGApps` [Mini+]
  * `NanoGApps` [Micro+]
  * `PicoGApps` [Nano+]


### Include or Exclude GApps

You can choose either the apps you WANT installed or the apps you DON'T WANT installed.

 - "Include" install: To select ONLY the apps you WANT installed, add the keyword `Include` to your gapps-config file. The installer will now install ONLY THOSE APPS you have listed in your gapps-config.
 - "Exclude" install: To select ONLY the apps you DON'T want installed, no keyword is necessary, because the default behavior is an Exclude install.

To use this feature, add the the keyword for each app you want to Include/Exclude inside your gapps-config file. The following is a sample "Include" gapps-config that contains all available app keywords -- using this gapps-config without modifications will install all apps the installer has available. You start with this file and comment out the apps you do not want installed:


```sh
Include

# Pico+
CalSync                # Install Google Calendar Sync (except if Google Calendar is being installed)
DialerFramework        # Install Dialer Framework
GoogleTTS              # Install Google Text-to-Speech (Micro+ on 5.0-, Pico+ on 6.0+)
PackageInstallerGoogle # Install Google Package Installer

# Nano+
BatteryUsage           # Install Device Health Services (7.1+)
FaceDetect             # Install Face Detect library for photo apps
FaceUnlock             # Install FaceUnlock
Search                 # Install Google Search (excluding excludes GoogleNow and PixelLauncher)
Speech                 # Install Offline Speech Files

# Micro+
CalendarGoogle         # Install Google Calendar
ExchangeGoogle         # Install Google Exchange Services
Gmail                  # Install Gmail
GoogleNow              # Install Google Now Launcher (requires Search)
# GoogleTTS              # Install Google Text-to-Speech (Micro+ on 5.0-, Pico+ on 6.0+)

# Mini+
CalculatorGoogle       # Install Google Calculator
ClockGoogle            # Install Google Clock
GooglePlus             # Install Google+
Maps                   # Install Google Maps
Messenger              # Install Android Messages (except on tablet devices)
Photos                 # Install Google Photos
TagGoogle              # Install Google NFC Tags
YouTube                # Install YouTube

# Full+
Books                  # Install Google Play Books
Chrome                 # Install Google Chrome Browser
CloudPrint             # Install Google Cloud Print
Docs                   # Install Google Docs
Drive                  # Install Google Drive
Fitness                # Install Google Fit
Keep                   # Install Google Keep
Movies                 # Install Google Play Movies & TV
Music                  # Install Google Play Music
NewsStand              # Install Google Play Newsstand
NewsWidget             # Install Google News & Weather
PlayGames              # Install Google Play Games
Sheets                 # Install Google Sheets
Slides                 # Install Google Slides
Talkback               # Install Google TalkBack

# Stock+
CameraGoogle           # Install Google Camera
ContactsGoogle         # Install Google Contacts
DialerGoogle           # Install Google Dialer
Duo                    # Install Google Duo
Hangouts               # Install Hangouts
KeyboardGoogle         # Install Google Keyboard
PixelIcons             # Install Google Pixel Icons
PixelLauncher          # Install Pixel Launcher (requires Search and Wallpapers)
PrintServiceGoogle     # Install Print Service Recommendation Service
StorageManagerGoogle   # Install Google Storage Manager
VRService              # Install Google VR Services
Wallpapers             # Install Wallpapers
WebViewGoogle          # Install Google Webview

# Super+
CarrierServices        # Install Carrier Services
DMAgent                # Install Google Apps Device Policy
Earth                  # Install Google Earth
GCS                    # Install Google Connectivity Services (excluding also excludes ProjectFi)
GooglePay              # Install Google Pay
Indic                  # Install Google Indic Keyboard
Japanese               # Install Google Japanese Input
Korean                 # Install Google Korean Input
Pinyin                 # Install Google Pinyin Input
ProjectFi              # Install Project Fi by Google
Street                 # Install Google Street View
Translate              # Install Google Translate
Zhuyin                 # Install Google Zhuyin Input
```


### Prevent automatic Stock removals

When installing a Google app that can replace a stock app, the stock app is automatically removed. For example, if you are installing Android Messages, then the Stock SMS app will automatically be removed.

To prevent the automatic removal of the stock apps when using the Open GApps Super/Stock package, type the keyword option preceded by a '+' as shown below:

```sh
+Browser       # Don't remove Stock Browser, even if Google Chrome is being installed
+CameraStock   # Don't remove Stock Camera, even if Google Camera is being installed
+Email         # Don't remove Stock Email, even if Gmail is being installed
+Gallery       # Don't remove Stock Gallery, even if Google Photos is being installed
+Launcher      # Don't remove Stock Launchers, even if Google Now Launcher is being installed
+MMS           # Don't remove Stock SMS app, even if Android Messages is being installed
+PicoTTS       # Don't remove PicoTTS, even if GoogleTTS is being installed
```

*(At the moment these are the only apps on which this feature works.)*


### Remove Stock apps

You can specify built-in (stock) apps you want removed. Stock removals function the same regardless of whether you're doing an "Include" or "Exclude" install.

Here are the vendors we support. Since different vendors use different names for their stock apps, some apps might remain unremoved if you are using another vendor.

 - AOSP
 - BLU
 - CyanogenMod
 - CypherOS (a.k.a AOSCP)
 - Flux
 - FlymeOS (BrowserIntl, Browser, CustomizeCenter, EasyLauncher, FileManager, FlymeLauncherIntl, FlymeLauncher, MzMPay, MzPay, MzInput, MzSetupWizard, MzUpdate, SystemUpdate, SystemUpdateAssistant, Weather)
 - Lenovo (packageinstaller)
 - LineageOS
 - Miui
 - MoKee (Nox launcher, YuBrowser)
 - Motorola
 - Omni (Apollo, Omni Deskclock2, OmniSwitch)
 - Paranoid Android

To use this feature, add the the keyword for each stock app you want removed, inside your gapps-config file. The following is a sample gapps-config that contains all available stock removal keywords -- using this gapps-config without modifications won't remove anything (that is not automatically removed, see below). You can start with this file and uncomment the apps you want removed:

```sh
# Remove apps (uncomment a line to remove the app)
# CMAccount               # Remove CM Account
# CMAudioFX               # Remove CM AudioFX
# CMBugReport             # Remove CM Bug Report
# CMFileManager           # Remove CM File Manager
# CMMusic                 # Remove CM Music
# CMScreenCast            # Remove CM ScreenCast
# CMSetupWizard           # Remove CM Setup Wizard (see Notes for CMSetupWizard)
# CMUpdater               # Remove CM Updater
# CMWallpapers            # Remove CM Wallpapers
# CMWeatherProvider       # Remove CM Weather Underground

# Bolt                    # Remove CypherOS Bolt Browser
# CameraX                 # Remove CypherOS Camera
# DashClock               # Remove DashClock Widget (found in certain ROMs)
# GalleryX                # Remove CypherOS Gallery
# Hexo                    # Remove Hexo Libre CM Theme
# LRecorder               # Remove LineageOS Recorder
# LSetupWizard            # Remove LineageOS Setup Wizard
# LUpdater                # Remove LineageOS Updater
# Logcat                  # Remove OmniROM MatLog
# MusicX                  # Remove CypherOS Music Player
# OmniSwitch              # Remove OmniSwitch recent apps switcher replacement

# BasicDreams             # Remove Basic Dreams Wallpaper
# Galaxy                  # Remove Galaxy (also known as BlackHole) Wallpaper
# HoloSpiral              # Remove Holo Spiral Wallpaper
# NoiseField              # Remove Noise Field Wallpaper
# Phasebeam               # Remove Phasebeam Wallpaper
# PhotoPhase              # Remove Photo Phase Wallpaper
# PhotoTable              # Remove Photo Table Wallpaper

# Browser                 # Remove Stock Browser
# CalculatorStock         # Remove Stock Calculator (automatically removed when Google Calculator is installed)
# CalendarStock           # Remove Stock Calendar (automatically removed when Google Calendar is installed)
# CameraStock             # Remove Stock Camera (Including CAF's camera application, Snap)
# ClockStock              # Remove Stock Desk Clock (automatically removed when Google Clock is installed)
# Email                   # Remove Stock Email Client
# ExchangeStock           # Remove Stock Exchange Services (automatically removed when Google Exchange Services is installed)
# FMRadio                 # Remove Stock FM Radio (not found on all devices or ROMs)
# Gallery                 # Remove Stock Gallery (automatically removed when Google Photos is installed)
# KeyboardStock           # Remove Stock Keyboard (automatically removed when Google Keyboard is installed)
# Launcher                # Remove Stock Launcher(s)
# LiveWallpapers          # Remove Stock Live Wallpapers
# LockClock               # Remove Stock Lockscreen Clock Widget
# MMS                     # Remove Stock SMS (automatically removed if Android Messages is installed)
# MzFileManager           # Remove Stock FlymeOS File Manager
# MzPay                   # Remove Stock FlymeOS Pay system (this service is only available in China)
# MzSetupWizard           # Remove Stock FlymeOS SetupWizard
# MzUpdater               # Remove Stock FlymeOS Updater
# MzWeather               # Remove Stock FlymeOS Weather (this service is only available in China)
# PicoTTS                 # Remove Stock PicoTTS
# PrintServiceStock       # Remove Stock Print Service Recommendation Service (automatically removed when Google Print Service Recommendation Service is installed)
# SimToolKit              # Remove Stock SimToolKit
# SoundRecorder           # Remove Stock Sound Recorder
# StorageManagerStock     # Remove Stock Storage Manager (automatically removed when Google Storage Manager is installed)
# Studio                  # Remove Stock Movie Studio
# SykoPath                # Remove SykoPath Layers Manager (found in certain ROMs)
# TagStock                # Remove Stock NFC Tags (automatically removed when Google NFC Tags is installed)
# Terminal                # Remove Stock Terminal
# Themes                  # Remove Stock Theme Engine (will break the Settings Entry and can cause unexpected reboots on some ROMs)
# VisualizationWallpapers # Remove Stock Visualization Wallpapers
# WhisperPush             # Remove Stock WhisperPush support
```

In addition to the Stock Removals above, you can remove ANY system app on your device or ROM, with the EXCEPTION of (core) apps that are part of Open GApps itself. To use this feature, enclose the name of the apk in parentheses inside your gapps-config file.

For example, to remove the Spare Parts app found in many ROMs, simply add `(SpareParts)` to your gapps-config. When using this feature, keep the following in mind:

 - Adding the .apk extension is not required (but will work).
 - Works for all apps in any system/app or system/priv-app subfolder.
 - Removes the entire contents of the folder containing the apk (including subfolders).
 - Removal is also added to the `addon.d` backup script so the removals will also be applied if you update your ROM.
 - Gives you the ability to do some really bad things to your device, so **DO A BACKUP** before trying.

_**WARNING**: Because this feature gives you the ability to remove files that may be important to the proper function of your device, it is only recommended for very experienced users who know what they are doing._


### Enable Google Assistant
Open GApps can add `ro.opa.eligible_device=true` to the build.prop file, to enable Google Assistant. By default this feature is not enabled, but it can be activated by adding the `GoogleAssistant` keyword.
If there is any line with `ro.opa.eligible_device` already in the build.prop it will NOT be overwritten.


### Force DPI Setting

Open GApps normally selects the correct DPI-optimized app that suits your device, based on the information that is supplied by recovery and otherwise found in default.prop or build.prop. Sometimes one might want to override this DPI setting, e.g. for testing, in those situations the keyword `forcedpiXXX` can be used, where XXX is replaced with one of the [valid default DPIs](http://developer.android.com/reference/android/util/DisplayMetrics.html) including: 120, 160, 213, 240, 260, 280, 300, 320, 340, 360, 400, 420, 480, 560, 640 or nodpi.


### Force New Camera

Open GApps normally detects if the device is deemed compatible with the _New Camera API_ based on fields specified in `build.prop` and a whitelist. If not deemed compatible, the newest Google Camera (version 3 and higher) will not be installed but the older version 2 instead (`googlecameralegacy`). To override this detection the `forcenewcamera` keyword can be used. Note: Google Camera version 3 does not work correctly on most non-Nexus devices.


### Skip Google's Swype Library Setting

The Stock keyboard does normally not support gesture typing. If Google Keyboard is not being installed, Open GApps installs by default Google's swype gesture libraries to the Stock keyboard. The libraries are installed in addition to the AOSP libraries. In some cases adding these libraries is unwanted behavior (there are few reports that recent these can conflict with certain ROMs). In those situations use the `skipswypelibs` keyword to skip the installation of these libraries (or remove them if previously installed).


### Substitute AOSP Library with Google's Swype Library Setting

The Stock keyboard does normally not support gesture typing. If Google Keyboard is not being installed, Open GApps installs by default Google's swype gesture libraries to the Stock keyboard. The libraries are installed in addition to the AOSP libraries. In some cases these gesture libraries only work if they are installed as a _replacement_ of the AOSP libraries (there are few reports that this is necessary with certain ROMs). In those situations use the `substituteswypelibs` keyword to replace the Stock libraries. (If you re-run the installation without the keyword, the AOSP libraries are restored to their original configuration).


### Skip updating vendor libraries

Open GApps by default updates certain libraries that are depended on by certain GApps (especially Face Unlock) that are stored in `/system/vendor` (or a `/vendor` partition via a symlink). To prevent GApps from touching (removing, adding or replacing) these vendor files use the `skipvendorlibs` keyword.


### Skip Smart Pre-ODEXing of APKs

On Marshmallow some ROMs are set to be extremely strict when verifying the APK. This can lead to de-odexed APKs to fail verification; because the included classes.dex is not present in the APK's MANIFEST. To avoid this potential issue, Open GApps by default pre-ODEXes these APKs on 6.0+. As positive side-effect this setting also improves the performance of these applications. A downside is that it occupies more disk-space on /system, because a copy of the classes.dex has to be kept for regenerating the ODEX when updating the ROM. To disable this feature use the keyword `NoPreODEX`. **THE PRE-ODEX FEATURE IS TEMPORARILY DISABLED BY DEFAULT; SEE BELOW HOW TO ENABLE**


### Enable Smart Pre-ODEXing of APKs

To enable Pre-ODEXing on ROMs the `PreODEX` can be used.


### Force Clean Install Setting

Open GApps normally detects if it's a clean install or an upgrade. This affects how installation of Google Camera is treated, it won't install those unless this is a clean install to avoid problems during upgrades. To ignore the detection and enforce clean install use `forceclean` keyword. Note: this setting is untested widely and may cause problems.


### Protection from stupidity

To prevent you from accidentally leaving yourself with no keyboard, Launcher, or MMS app when you start your device, the installer WILL NOT ALLOW you to remove the Stock Keyboard, Launcher, or MMS app if you are not also installing a Google version of these apps. You can, however, override this protection by adding the keyword `Override` to your gapps-config. Be very careful when using this option and make certain you have a replacement app already installed on your device before using this option. This keyword can also be used to override the automatic selection of `WebViewStub` over `WebViewGoogle` if `Chrome` is being installed.


---

## Links to GApps on the Play Store

 - [Android Messages](https://play.google.com/store/apps/details?id=com.google.android.apps.messaging)
 - [Exchange Services](https://play.google.com/store/apps/details?id=com.google.android.gm.exchange)
 - [Carrier Services](https://play.google.com/store/apps/details?id=com.google.android.ims)
 - [Gmail](https://play.google.com/store/apps/details?id=com.google.android.gm)
 - [Google Apps Device Policy](https://play.google.com/store/apps/details?id=com.google.android.apps.enterprise.dmagent)
 - [Google Calculator](https://play.google.com/store/apps/details?id=com.google.android.calculator)
 - [Google Calendar](https://play.google.com/store/apps/details?id=com.google.android.calendar)
 - [Google Camera](https://play.google.com/store/apps/details?id=com.google.android.GoogleCamera)
 - [Google Chrome](https://play.google.com/store/apps/details?id=com.android.chrome)
 - [Google Clock](https://play.google.com/store/apps/details?id=com.google.android.deskclock)
 - [Google Cloud Print](https://play.google.com/store/apps/details?id=com.google.android.apps.cloudprint)
 - [Google Connectivity Services](https://play.google.com/store/apps/details?id=com.google.android.apps.gcs)
 - [Google Contacts](https://play.google.com/store/apps/details?id=com.google.android.contacts)
 - [Google Dialer](https://play.google.com/store/apps/details?id=com.google.android.dialer)
 - [Google Duo](https://play.google.com/store/apps/details?id=com.google.android.apps.tachyon)
 - [Google Docs](https://play.google.com/store/apps/details?id=com.google.android.apps.docs.editors.docs)
 - [Google Drive](https://play.google.com/store/apps/details?id=com.google.android.apps.docs)
 - [Google Earth](https://play.google.com/store/apps/details?id=com.google.earth)
 - [Google Fit](https://play.google.com/store/apps/details?id=com.google.android.apps.fitness)
 - [Google Indic Keyboard](https://play.google.com/store/apps/details?id=com.google.android.apps.inputmethod.hindi)
 - [Google Japanese Input](https://play.google.com/store/apps/details?id=com.google.android.inputmethod.japanese)
 - [Google Keep](https://play.google.com/store/apps/details?id=com.google.android.keep)
 - [Google Keyboard](https://play.google.com/store/apps/details?id=com.google.android.inputmethod.latin)
 - [Google Korean Input](https://play.google.com/store/apps/details?id=com.google.android.inputmethod.korean)
 - [Google Maps](https://play.google.com/store/apps/details?id=com.google.android.apps.maps)
 - [Google News & Weather](https://play.google.com/store/apps/details?id=com.google.android.apps.genie.geniewidget)
 - [Google Now Launcher](https://play.google.com/store/apps/details?id=com.google.android.launcher)
 - [Google Pay](https://play.google.com/store/apps/details?id=com.google.android.apps.walletnfcrel)
 - [Google Photos](https://play.google.com/store/apps/details?id=com.google.android.apps.photos)
 - [Google Pinyin Input](https://play.google.com/store/apps/details?id=com.google.android.inputmethod.pinyin)
 - [Google Play Books](https://play.google.com/store/apps/details?id=com.google.android.apps.books)
 - [Google Play Games](https://play.google.com/store/apps/details?id=com.google.android.play.games)
 - [Google Play Movies & TV](https://play.google.com/store/apps/details?id=com.google.android.videos)
 - [Google Play Music](https://play.google.com/store/apps/details?id=com.google.android.music)
 - [Google Play Newsstand](https://play.google.com/store/apps/details?id=com.google.android.apps.magazines)
 - [Google Search](https://play.google.com/store/apps/details?id=com.google.android.googlequicksearchbox)
 - [Google Sheets](https://play.google.com/store/apps/details?id=com.google.android.apps.docs.editors.sheets)
 - [Google Slides](https://play.google.com/store/apps/details?id=com.google.android.apps.docs.editors.slides)
 - [Google Street View](https://play.google.com/store/apps/details?id=com.google.android.street)
 - [Google TalkBack](https://play.google.com/store/apps/details?id=com.google.android.marvin.talkback)
 - [Google Text-to-Speech](https://play.google.com/store/apps/details?id=com.google.android.tts)
 - [Google Translate](https://play.google.com/store/apps/details?id=com.google.android.apps.translate)
 - [Google VR Services](https://play.google.com/store/apps/details?id=com.google.vr.vrcore)
 - [Google Webview Stub](https://play.google.com/store/apps/details?id=com.google.android.webview)
 - [Google Webview](https://play.google.com/store/apps/details?id=com.google.android.webview)
 - [Google Zhuyin Input](https://play.google.com/store/apps/details?id=com.google.android.apps.inputmethod.zhuyin)
 - [Google+](https://play.google.com/store/apps/details?id=com.google.android.apps.plus)
 - [Hangouts](https://play.google.com/store/apps/details?id=com.google.android.talk)
 - [Pixel Launcher](https://play.google.com/store/apps/details?id=com.google.android.apps.nexuslauncher)
 - [Project Fi by Google](https://play.google.com/store/apps/details?id=com.google.android.apps.tycho)
 - [Wallpapers](https://play.google.com/store/apps/details?id=com.google.android.apps.wallpaper)
 - [YouTube](https://play.google.com/store/apps/details?id=com.google.android.youtube)
