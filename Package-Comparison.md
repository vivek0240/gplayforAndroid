* Android 11: we have released the Pico and Nano versions only @ the present. Other variants will be available as soon as we confirm that everything's working properly.
* Google removed the `Trusted Face` (FaceUnlock) feature for security reasons (see [this post](https://www.androidpolice.com/2019/09/04/trusted-face-smart-unlock-method-has-been-removed-from-android-devices/)). We've removed the corresponding code for the `FaceDetect` and `FaceUnlock` for all platforms.
* Not included in this table: [[Aroma|Aroma Package]] & [[TVStock|TVStock Package]]

|Legend | Description |
|:-------:|------------|
|X      | Installs application by default |
|O      | Replaces the Stock/AOSP version of the application by default |
|\+    | Only installed if Google Calendar is NOT installed |
|4.4   | Application is installed on Android 4.4 only |
|7.1   | Application is installed on Android 7.1 only |

|Application Name    |gapps-config keyword|p<br>i<br>c<br>o|n<br>a<br>n<br>o|m<br>i<br>c<br>r<br>o|m<br>i<br>n<br>i|f<br>u<br>l<br>l|s<br>t<br>o<br>c<br>k|s<br>u<br>p<br>e<br>r|
|:-----------------:|:-------------:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|
|            Google Play Services             |                                   |  X  |  X  |  X  |  X  |  X  |  X  |  X  |
|              Google Play Store              |                                   |  X  |  X  |  X  |  X  |  X  |  X  |  X  |
|             Google System Base              |                                   |  X  |  X  |  X  |  X  |  X  |  X  |  X  |
|              Android Auto stub⁵             |        ``GearheadStub``           |  X  |  X  |  X  |  X  |  X  |  X  |  X  |
|            Google Calendar Sync             |            ``CalSync``            |  X  |  X  | \+  | \+  | \+  | \+  | \+  |
|              Dialer Framework               |        ``DialerFramework``        |  X  |  X  |  X  |  X  |  X  |  X  |  X  |
|            Google Text-to-Speech            |           ``GoogleTTS``           |  X  |  X  |  X  |  X  |  X  |  O  |  O  |
|          Google Package Installer           |    ``PackageInstallerGoogle``     |  O  |  O  |  O  |  O  |  O  |  O  |  O  |
|                   Sounds                    |          ``SoundPicker``          |     |  X  |  X  |  X  |  X  |  X  |  X  |
|           Device Health Services            |         ``BatteryUsage``          |     |  X  |  X  |  X  |  X  |  X  |  X  |
|                Google Markup                |            ``Markup``             |     |  X  |  X  |  X  |  X  |  X  |  X  |
|             Google App (Search)             |            ``Search``             |     |  X  |  X  |  X  |  X  |  X  |  X  |
|            Offline Speech Files             |            ``Speech``             |     |  X  |  X  |  X  |  X  |  X  |  X  |
|          Google Digital Wellbeing           |           ``Wellbeing``           |     |  X  |  X  |  X  |  X  |  X  |  X  |
|              Actions Services²              |        ``ActionsServices``        |     |     |  X  |  X  |  X  |  X  |  X  |
|              Google Calendar¹               |        ``CalendarGoogle``         |     |     |  O  |  O  |  O  |  O  |  O  |
|          Google Exchange Services¹          |        ``ExchangeGoogle``         |     |     |  O  |  O  |  O  |  O  |  O  |
|                    Gmail                    |             ``Gmail``             |     |     |  X  |  X  |  X  |  O  |  O  |
|            Google Now Launcher²             |           ``GoogleNow``           |     |     | 4.4 | 4.4 | 4.4 | 4.4 | 4.4 |
|                 Pixel Icons                 |          ``PixelIcons``           |     |     | 7.1 | 7.1 | 7.1 | 7.1 | 7.1 |
|               Pixel Launcher²               |         ``PixelLauncher``         |     |     |  O  |  O  |  O  |  O  |  O  |
|              Google Wallpapers              |          ``Wallpapers``           |     |     |  O  |  O  |  O  |  O  |  O  |
|             Google Calculator¹              |       ``CalculatorGoogle``        |     |     |     |  O  |  O  |  O  |  O  |
|              Carrier Services               |        ``CarrierServices``        |     |     |     |  X  |  X  |  X  |  X  |
|                Google Clock¹                |          ``ClockGoogle``          |     |     |     |  O  |  O  |  O  |  O  |
|                 Google Maps                 |             ``Maps``              |     |     |     |  X  |  X  |  X  |  X  |
|              Google Messages¹               |           ``Messenger``           |     |     |     |  O  |  O  |  O  |  O  |
|                Google Photos                |            ``Photos``             |     |     |     |  X  |  X  |  O  |  O  |
|                Google Tags¹                 |           ``TagGoogle``           |     |     |     |  O  |  O  |  O  |  O  |
|                   YouTube                   |            ``YouTube``            |     |     |     |  X  |  X  |  X  |  X  |
|              Google Play Books              |             ``Books``             |     |     |     |     |  X  |  X  |  X  |
|                Google Chrome⁴               |            ``Chrome``             |     |     |     |     |  X  |  O  |  O  |
|                 Cloud Print                 |          ``CloudPrint``           |     |     |     |     |  X  |  X  |  X  |
|                Google Drive                 |             ``Drive``             |     |     |     |     |  X  |  X  |  X  |
|              Google Keep Notes              |             ``Keep``              |     |     |     |     |  X  |  X  |  X  |
|           Google Play Movies & TV           |            ``Movies``             |     |     |     |     |  X  |  X  |  X  |
|              Google Play Music              |             ``Music``             |     |     |     |     |  X  |  X  |  X  |
|                 Google News                 |           ``Newsstand``           |     |     |     |     |  X  |  X  |  X  |
|              Google Play Games              |           ``PlayGames``           |     |     |     |     |  X  |  X  |  X  |
|         Google Accessibility Suite          |           ``TalkBack``            |     |     |     |     |  X  |  X  |  X  |
|               Google Recorder               |           ``Recorder``            |     |     |     |     |  X  |  X  |  X  |
|                Android Auto                 |          ``AndroidAuto``          |     |     |     |     |     |  X  |  X  |
|               Google Camera¹                |         ``CameraGoogle``          |     |     |     |     |     |  O  |  O  |
|              Google Contacts¹               |        ``ContactsGoogle``         |     |     |     |     |     |  O  |  O  |
|                Google Phone²                |         ``DialerGoogle``          |     |     |     |     |     |  X  |  X  |
|                 Google Duo                  |              ``Duo``              |     |     |     |     |     |  X  |  X  |
|                 Google Pay                  |           ``GooglePay``           |     |     |     |     |     |  X  |  X  |
|              Google Keyboard¹               |        ``KeyboardGoogle``         |     |     |     |     |     |  O  |  O  |
|     Google Print Recommendation Service     |      ``PrintServiceGoogle``       |     |     |     |     |     |  O  |  O  |
|            Google Smart Storage             |     ``StorageManagerGoogle``      |     |     |     |     |     |  O  |  O  |
|              Google Translate               |           ``Translate``           |     |     |     |     |     |  X  |  X  |
|             Google VR Services              |           ``VRService``           |     |     |     |     |     |  X  |  X  |
|           Android System Webview¹⁴          |``WebViewGoogle`` ``WebViewStub``³ |     |     |     |     |     |  O  |  O  |
|               Better Together               |        ``BetterTogether``         |     |     |     |     |     |     |  X  |
|          Google Apps Device Policy          |            ``DMAgent``            |     |     |     |     |     |     |  X  |
|                 Google Docs                 |             ``Docs``              |     |     |     |     |     |     |  X  |
|                Google Earth                 |             ``Earth``             |     |     |     |     |     |     |  X  |
|                 Google Fit                  |            ``Fitness``            |     |     |     |     |     |     |  X  |
|        Google Connectivity Services         |              ``GCS``              |     |     |     |     |     |     |  X  |
|               Google Hangouts               |           ``Hangouts``            |     |     |     |     |     |     |  X  |
|            Google Indic Keyboard            |             ``Indic``             |     |     |     |     |     |     |  X  |
|            Google Japanese Input            |           ``Japanese``            |     |     |     |     |     |     |  X  |
|             Google Korean Input             |            ``Korean``             |     |     |     |     |     |     |  X  |
|             Google Pinyin Input             |            ``Pinyin``             |     |     |     |     |     |     |  X  |
|                 Project Fi²                 |           ``ProjectFi``           |     |     |     |     |     |     |  X  |
|                Google Sheets                |            ``Sheets``             |     |     |     |     |     |     |  X  |
|                Google Slides                |            ``Slides``             |     |     |     |     |     |     |  X  |
|             Google Street View              |            ``Street``             |     |     |     |     |     |     |  X  |
|             Google Zhuyin Input             |            ``Zhuyin``             |     |     |     |     |     |     |  X  |

* ¹ By default replaces the Stock/AOSP version of the application included in the ROM to avoid problems
* ² Google Dialer depends on Dialer Framework; Google Now depends on Search; Pixel Launcher depends on Actions Services, Search and Wallpapers; Project Fi depends on GCS
* ³ Google WebView Stub only installs a placeholder APK of Google WebView that needs to be updated to function. Requires Android 7.0 or higher
* ⁴ Google Chrome and WebView require Trichrome Library starting with Android 10+, so it'll be installed with these
* ⁵ Android Auto stub only installs a placeholder APK of Android Auto that needs to be updated to function. Requires Android 10 or higher.
* Note that some applications are only available on higher Android versions or compatible hardware


---

## Links to GApps on the Play Store

 - [Google LLC - developer's page](https://play.google.com/store/apps/dev?id=5700313618786177705)
 - [Android Auto](https://play.google.com/store/apps/details?id=com.google.android.projection.gearhead)
 - [Android Accessibility Suite (Talkback)](https://play.google.com/store/apps/details?id=com.google.android.marvin.talkback)
 - [Exchange Services](https://play.google.com/store/apps/details?id=com.google.android.gm.exchange)
 - [Carrier Services](https://play.google.com/store/apps/details?id=com.google.android.ims)
 - [Gboard (Google Keyboard)](https://play.google.com/store/apps/details?id=com.google.android.inputmethod.latin)
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
 - [Google Device Health Services](https://play.google.com/store/apps/details?id=com.google.android.apps.turbo)
 - [Google Dialer](https://play.google.com/store/apps/details?id=com.google.android.dialer)
 - [Google Digital Wellbeing](https://play.google.com/store/apps/details?id=com.google.android.apps.wellbeing)
 - [Google Duo](https://play.google.com/store/apps/details?id=com.google.android.apps.tachyon)
 - [Google Docs](https://play.google.com/store/apps/details?id=com.google.android.apps.docs.editors.docs)
 - [Google Drive](https://play.google.com/store/apps/details?id=com.google.android.apps.docs)
 - [Google Earth](https://play.google.com/store/apps/details?id=com.google.earth)
 - [Google Fit](https://play.google.com/store/apps/details?id=com.google.android.apps.fitness)
 - [Google Indic Keyboard](https://play.google.com/store/apps/details?id=com.google.android.apps.inputmethod.hindi)
 - [Google Japanese Input](https://play.google.com/store/apps/details?id=com.google.android.inputmethod.japanese)
 - [Google Keep Notes](https://play.google.com/store/apps/details?id=com.google.android.keep)
 - [Google Korean Input](https://play.google.com/store/apps/details?id=com.google.android.inputmethod.korean)
 - [Google Maps](https://play.google.com/store/apps/details?id=com.google.android.apps.maps)
 - [Google Messages](https://play.google.com/store/apps/details?id=com.google.android.apps.messaging)
 - [Google News](https://play.google.com/store/apps/details?id=com.google.android.apps.magazines)
 - [Google Now Launcher](https://play.google.com/store/apps/details?id=com.google.android.launcher)
 - [Google Pay](https://play.google.com/store/apps/details?id=com.google.android.apps.walletnfcrel)
 - [Google Photos](https://play.google.com/store/apps/details?id=com.google.android.apps.photos)
 - [Google Pinyin Input](https://play.google.com/store/apps/details?id=com.google.android.inputmethod.pinyin)
 - [Google Play Books](https://play.google.com/store/apps/details?id=com.google.android.apps.books)
 - [Google Play Games](https://play.google.com/store/apps/details?id=com.google.android.play.games)
 - [Google Play Movies & TV](https://play.google.com/store/apps/details?id=com.google.android.videos)
 - [Google Play Music](https://play.google.com/store/apps/details?id=com.google.android.music)
 - [Google Search](https://play.google.com/store/apps/details?id=com.google.android.googlequicksearchbox)
 - [Google Sheets](https://play.google.com/store/apps/details?id=com.google.android.apps.docs.editors.sheets)
 - [Google Slides](https://play.google.com/store/apps/details?id=com.google.android.apps.docs.editors.slides)
 - [Google Sounds](https://play.google.com/store/apps/details?id=com.google.android.soundpicker)
 - [Google Street View](https://play.google.com/store/apps/details?id=com.google.android.street)
 - [Google Text-to-Speech](https://play.google.com/store/apps/details?id=com.google.android.tts)
 - [Google Translate](https://play.google.com/store/apps/details?id=com.google.android.apps.translate)
 - [Google VR Services](https://play.google.com/store/apps/details?id=com.google.vr.vrcore)
 - [Google Webview Stub](https://play.google.com/store/apps/details?id=com.google.android.webview)
 - [Google Webview](https://play.google.com/store/apps/details?id=com.google.android.webview)
 - [Google Zhuyin Input](https://play.google.com/store/apps/details?id=com.google.android.apps.inputmethod.zhuyin)
 - [Google+](https://play.google.com/store/apps/details?id=com.google.android.apps.plus)
 - [Hangouts](https://play.google.com/store/apps/details?id=com.google.android.talk)
 - [Pixel Launcher](https://play.google.com/store/apps/details?id=com.google.android.apps.nexuslauncher)
 - [Project Fi](https://play.google.com/store/apps/details?id=com.google.android.apps.tycho)
 - [Recorder](https://play.google.com/store/apps/details?id=com.google.android.apps.recorder)
 - [Wallpapers](https://play.google.com/store/apps/details?id=com.google.android.apps.wallpaper)
 - [YouTube](https://play.google.com/store/apps/details?id=com.google.android.youtube)
