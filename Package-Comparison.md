
<div class="container-xl clearfix new-discussion-timeline px-3 px-md-4 px-lg-5">

<div class="repository-content ">

<div id="wiki-wrapper" class="page">

<div class="d-flex flex-column flex-md-row gh-header">

# Package Comparison

<div id="wiki-content" class="mt-4">

<div class="gutter-condensed gutter-lg flex-column flex-md-row d-flex">

<div class="flex-shrink-0 col-12 col-md-9 mb-4 mb-md-0">

<div id="wiki-body" class="gollum-markdown-content">

<div class="markdown-body">

*   Google removed the `Trusted Face` (FaceUnlock) feature for security reasons (see [this post](https://web.archive.org/web/20201112003349/https://www.androidpolice.com/2019/09/04/trusted-face-smart-unlock-method-has-been-removed-from-android-devices/)). We've removed the corresponding code for the `FaceDetect` and `FaceUnlock` for all platforms.
*   Not included in this table: [Aroma](/web/20201112003349/https://github.com/opengapps/opengapps/wiki/Aroma-Package) & [TVStock](/web/20201112003349/https://github.com/opengapps/opengapps/wiki/TVStock-Package)

<table role="table">

<thead>

<tr>

<th align="center">Legend</th>

<th>Description</th>

</tr>

</thead>

<tbody>

<tr>

<td align="center">X</td>

<td>Installs application by default</td>

</tr>

<tr>

<td align="center">O</td>

<td>Replaces the Stock/AOSP version of the application by default</td>

</tr>

<tr>

<td align="center">+</td>

<td>Only installed if Google Calendar is NOT installed</td>

</tr>

<tr>

<td align="center">4.4</td>

<td>Application is installed on Android 4.4 only</td>

</tr>

<tr>

<td align="center">7.1</td>

<td>Application is installed on Android 7.1 only</td>

</tr>

</tbody>

</table>

<table role="table">

<thead>

<tr>

<th align="center">Application Name</th>

<th align="center">gapps-config keyword</th>

<th align="center">p  
i  
c  
o</th>

<th align="center">n  
a  
n  
o</th>

<th align="center">m  
i  
c  
r  
o</th>

<th align="center">m  
i  
n  
i</th>

<th align="center">f  
u  
l  
l</th>

<th align="center">s  
t  
o  
c  
k</th>

<th align="center">s  
u  
p  
e  
r</th>

</tr>

</thead>

<tbody>

<tr>

<td align="center">Google Play Services</td>

<td align="center"></td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

</tr>

<tr>

<td align="center">Google Play Store</td>

<td align="center"></td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

</tr>

<tr>

<td align="center">Google System Base</td>

<td align="center"></td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

</tr>

<tr>

<td align="center">Google Calendar Sync</td>

<td align="center">`CalSync`</td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">+</td>

<td align="center">+</td>

<td align="center">+</td>

<td align="center">+</td>

<td align="center">+</td>

</tr>

<tr>

<td align="center">Dialer Framework</td>

<td align="center">`DialerFramework`</td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

</tr>

<tr>

<td align="center">Google Text-to-Speech</td>

<td align="center">`GoogleTTS`</td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">O</td>

<td align="center">O</td>

</tr>

<tr>

<td align="center">Google Package Installer</td>

<td align="center">`PackageInstallerGoogle`</td>

<td align="center">O</td>

<td align="center">O</td>

<td align="center">O</td>

<td align="center">O</td>

<td align="center">O</td>

<td align="center">O</td>

<td align="center">O</td>

</tr>

<tr>

<td align="center">Sounds</td>

<td align="center">`SoundPicker`</td>

<td align="center"></td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

</tr>

<tr>

<td align="center">Device Health Services</td>

<td align="center">`BatteryUsage`</td>

<td align="center"></td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

</tr>

<tr>

<td align="center">Google Markup</td>

<td align="center">`Markup`</td>

<td align="center"></td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

</tr>

<tr>

<td align="center">Google App (Search)</td>

<td align="center">`Search`</td>

<td align="center"></td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

</tr>

<tr>

<td align="center">Offline Speech Files</td>

<td align="center">`Speech`</td>

<td align="center"></td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

</tr>

<tr>

<td align="center">Google Digital Wellbeing</td>

<td align="center">`Wellbeing`</td>

<td align="center"></td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

</tr>

<tr>

<td align="center">Actions Services²</td>

<td align="center">`ActionsServices`</td>

<td align="center"></td>

<td align="center"></td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

</tr>

<tr>

<td align="center">Google Calendar¹</td>

<td align="center">`CalendarGoogle`</td>

<td align="center"></td>

<td align="center"></td>

<td align="center">O</td>

<td align="center">O</td>

<td align="center">O</td>

<td align="center">O</td>

<td align="center">O</td>

</tr>

<tr>

<td align="center">Google Exchange Services¹</td>

<td align="center">`ExchangeGoogle`</td>

<td align="center"></td>

<td align="center"></td>

<td align="center">O</td>

<td align="center">O</td>

<td align="center">O</td>

<td align="center">O</td>

<td align="center">O</td>

</tr>

<tr>

<td align="center">Gmail</td>

<td align="center">`Gmail`</td>

<td align="center"></td>

<td align="center"></td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">O</td>

<td align="center">O</td>

</tr>

<tr>

<td align="center">Google Now Launcher²</td>

<td align="center">`GoogleNow`</td>

<td align="center"></td>

<td align="center"></td>

<td align="center">4.4</td>

<td align="center">4.4</td>

<td align="center">4.4</td>

<td align="center">4.4</td>

<td align="center">4.4</td>

</tr>

<tr>

<td align="center">Pixel Icons</td>

<td align="center">`PixelIcons`</td>

<td align="center"></td>

<td align="center"></td>

<td align="center">7.1</td>

<td align="center">7.1</td>

<td align="center">7.1</td>

<td align="center">7.1</td>

<td align="center">7.1</td>

</tr>

<tr>

<td align="center">Pixel Launcher²</td>

<td align="center">`PixelLauncher`</td>

<td align="center"></td>

<td align="center"></td>

<td align="center">O</td>

<td align="center">O</td>

<td align="center">O</td>

<td align="center">O</td>

<td align="center">O</td>

</tr>

<tr>

<td align="center">Google Wallpapers</td>

<td align="center">`Wallpapers`</td>

<td align="center"></td>

<td align="center"></td>

<td align="center">O</td>

<td align="center">O</td>

<td align="center">O</td>

<td align="center">O</td>

<td align="center">O</td>

</tr>

<tr>

<td align="center">Google Calculator¹</td>

<td align="center">`CalculatorGoogle`</td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center">O</td>

<td align="center">O</td>

<td align="center">O</td>

<td align="center">O</td>

</tr>

<tr>

<td align="center">Carrier Services</td>

<td align="center">`CarrierServices`</td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

</tr>

<tr>

<td align="center">Google Clock¹</td>

<td align="center">`ClockGoogle`</td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center">O</td>

<td align="center">O</td>

<td align="center">O</td>

<td align="center">O</td>

</tr>

<tr>

<td align="center">Google Maps</td>

<td align="center">`Maps`</td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

</tr>

<tr>

<td align="center">Google Messages¹</td>

<td align="center">`Messenger`</td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center">O</td>

<td align="center">O</td>

<td align="center">O</td>

<td align="center">O</td>

</tr>

<tr>

<td align="center">Google Photos</td>

<td align="center">`Photos`</td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">O</td>

<td align="center">O</td>

</tr>

<tr>

<td align="center">Google Tags¹</td>

<td align="center">`TagGoogle`</td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center">O</td>

<td align="center">O</td>

<td align="center">O</td>

<td align="center">O</td>

</tr>

<tr>

<td align="center">YouTube</td>

<td align="center">`YouTube`</td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

</tr>

<tr>

<td align="center">Google Play Books</td>

<td align="center">`Books`</td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

</tr>

<tr>

<td align="center">Google Chrome⁴</td>

<td align="center">`Chrome`</td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center">X</td>

<td align="center">O</td>

<td align="center">O</td>

</tr>

<tr>

<td align="center">Cloud Print</td>

<td align="center">`CloudPrint`</td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

</tr>

<tr>

<td align="center">Google Drive</td>

<td align="center">`Drive`</td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

</tr>

<tr>

<td align="center">Google Keep Notes</td>

<td align="center">`Keep`</td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

</tr>

<tr>

<td align="center">Google Play Movies & TV</td>

<td align="center">`Movies`</td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

</tr>

<tr>

<td align="center">Google Play Music</td>

<td align="center">`Music`</td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

</tr>

<tr>

<td align="center">Google News</td>

<td align="center">`Newsstand`</td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

</tr>

<tr>

<td align="center">Google Play Games</td>

<td align="center">`PlayGames`</td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

</tr>

<tr>

<td align="center">Google Accessibility Suite</td>

<td align="center">`TalkBack`</td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

</tr>

<tr>

<td align="center">Google Recorder</td>

<td align="center">`Recorder`</td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center">X</td>

<td align="center">X</td>

<td align="center">X</td>

</tr>

<tr>

<td align="center">Android Auto</td>

<td align="center">`AndroidAuto`</td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center">X</td>

<td align="center">X</td>

</tr>

<tr>

<td align="center">Google Camera¹</td>

<td align="center">`CameraGoogle`</td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center">O</td>

<td align="center">O</td>

</tr>

<tr>

<td align="center">Google Contacts¹</td>

<td align="center">`ContactsGoogle`</td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center">O</td>

<td align="center">O</td>

</tr>

<tr>

<td align="center">Google Phone²</td>

<td align="center">`DialerGoogle`</td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center">X</td>

<td align="center">X</td>

</tr>

<tr>

<td align="center">Google Duo</td>

<td align="center">`Duo`</td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center">X</td>

<td align="center">X</td>

</tr>

<tr>

<td align="center">Google Pay</td>

<td align="center">`GooglePay`</td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center">X</td>

<td align="center">X</td>

</tr>

<tr>

<td align="center">Google Keyboard¹</td>

<td align="center">`KeyboardGoogle`</td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center">O</td>

<td align="center">O</td>

</tr>

<tr>

<td align="center">Google Print Recommendation Service</td>

<td align="center">`PrintServiceGoogle`</td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center">O</td>

<td align="center">O</td>

</tr>

<tr>

<td align="center">Google Smart Storage</td>

<td align="center">`StorageManagerGoogle`</td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center">O</td>

<td align="center">O</td>

</tr>

<tr>

<td align="center">Google Translate</td>

<td align="center">`Translate`</td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center">X</td>

<td align="center">X</td>

</tr>

<tr>

<td align="center">Google VR Services</td>

<td align="center">`VRService`</td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center">X</td>

<td align="center">X</td>

</tr>

<tr>

<td align="center">Android System Webview¹⁴</td>

<td align="center">`WebViewGoogle` `WebViewStub`³</td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center">O</td>

<td align="center">O</td>

</tr>

<tr>

<td align="center">Better Together</td>

<td align="center">`BetterTogether`</td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center">X</td>

</tr>

<tr>

<td align="center">Google Apps Device Policy</td>

<td align="center">`DMAgent`</td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center">X</td>

</tr>

<tr>

<td align="center">Google Docs</td>

<td align="center">`Docs`</td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center">X</td>

</tr>

<tr>

<td align="center">Google Earth</td>

<td align="center">`Earth`</td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center">X</td>

</tr>

<tr>

<td align="center">Google Fit</td>

<td align="center">`Fitness`</td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center">X</td>

</tr>

<tr>

<td align="center">Google Connectivity Services</td>

<td align="center">`GCS`</td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center">X</td>

</tr>

<tr>

<td align="center">Google Hangouts</td>

<td align="center">`Hangouts`</td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center">X</td>

</tr>

<tr>

<td align="center">Google Indic Keyboard</td>

<td align="center">`Indic`</td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center">X</td>

</tr>

<tr>

<td align="center">Google Japanese Input</td>

<td align="center">`Japanese`</td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center">X</td>

</tr>

<tr>

<td align="center">Google Korean Input</td>

<td align="center">`Korean`</td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center">X</td>

</tr>

<tr>

<td align="center">Google Pinyin Input</td>

<td align="center">`Pinyin`</td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center">X</td>

</tr>

<tr>

<td align="center">Project Fi²</td>

<td align="center">`ProjectFi`</td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center">X</td>

</tr>

<tr>

<td align="center">Google Sheets</td>

<td align="center">`Sheets`</td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center">X</td>

</tr>

<tr>

<td align="center">Google Slides</td>

<td align="center">`Slides`</td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center">X</td>

</tr>

<tr>

<td align="center">Google Street View</td>

<td align="center">`Street`</td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center">X</td>

</tr>

<tr>

<td align="center">Google Zhuyin Input</td>

<td align="center">`Zhuyin`</td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center"></td>

<td align="center">X</td>

</tr>

</tbody>

</table>

*   ¹ By default replaces the Stock/AOSP version of the application included in the ROM to avoid problems
*   ² Google Dialer depends on Dialer Framework; Google Now depends on Search; Pixel Launcher depends on Actions Services, Search and Wallpapers; Project Fi depends on GCS
*   ³ Google WebView Stub only installs a placeholder APK of Google WebView that needs to be updated to function. Requires Android 7.0 or higher
*   ⁴ Google Chrome and WebView require Trichrome Library starting with Android 10+, so it'll be installed with these
*   Note that some applications are only available on higher Android versions or compatible hardware

<div id="wiki-footer" class="mt-5 mb-0 wiki-footer gollum-markdown-content">

<div class="Box Box--condensed bg-gray box-shadow">

<div class="Box-body  markdown-body">

### [](#the-open-gapps-project)The Open GApps Project

[**Download**](https://web.archive.org/web/20201112003349/https://opengapps.org/#downloadsection) / [**Support**](https://web.archive.org/web/20201112003349/https://opengapps.org/#supportsection) / [**About**](https://web.archive.org/web/20201112003349/https://opengapps.org/#aboutsection) / [**FAQ**](https://web.archive.org/web/20201112003349/https://github.com/opengapps/opengapps/wiki/FAQ)

</div>

</div>

</div>

</div>

</div>

<div class="flex-shrink-0 col-12 col-md-3">

<div class="wiki-rightbar">

<div id="wiki-pages-box" class="mb-4 wiki-pages-box js-wiki-pages-box" role="navigation">

<div class="Box Box--condensed box-shadow">

<div class="Box-header js-wiki-toggle-collapse" style="cursor: pointer">

### Pages <span title="30" class="Counter Counter--gray ">30</span>

</div>

<div class="d-none js-wiki-sidebar-toggle-display">

<div class="filter-bar"><input type="text" id="wiki-pages-filter" class="form-control input-sm input-block js-filterable-field" placeholder="Find a Page…" aria-label="Find a Page…"></div>

*   **[Home](/web/20201112003349/https://github.com/opengapps/opengapps/wiki)**
*   **[Advanced Features and Options](/web/20201112003349/https://github.com/opengapps/opengapps/wiki/Advanced-Features-and-Options)**
*   **[Aroma Package](/web/20201112003349/https://github.com/opengapps/opengapps/wiki/Aroma-Package)**
*   **[FAQ](/web/20201112003349/https://github.com/opengapps/opengapps/wiki/FAQ)**
*   **[Full Package](/web/20201112003349/https://github.com/opengapps/opengapps/wiki/Full-Package)**
*   **[gapps‐config for OnePlus X's OxygenOS](/web/20201112003349/https://github.com/opengapps/opengapps/wiki/gapps%E2%80%90config-for-OnePlus-X's-OxygenOS)**
*   **[Get Involved](/web/20201112003349/https://github.com/opengapps/opengapps/wiki/Get-Involved)**
*   **[h910101](/web/20201112003349/https://github.com/opengapps/opengapps/wiki/h910101)**
*   **[Hotlinking to OpenGApps.org](/web/20201112003349/https://github.com/opengapps/opengapps/wiki/Hotlinking-to-OpenGApps.org)**
*   **[Micro Package](/web/20201112003349/https://github.com/opengapps/opengapps/wiki/Micro-Package)**
*   **[Mini Package](/web/20201112003349/https://github.com/opengapps/opengapps/wiki/Mini-Package)**
*   **[Nano Package](/web/20201112003349/https://github.com/opengapps/opengapps/wiki/Nano-Package)**
*   **[New OS](/web/20201112003349/https://github.com/opengapps/opengapps/wiki/New-OS)**
*   **[Notes for Android 10.x](/web/20201112003349/https://github.com/opengapps/opengapps/wiki/Notes-for-Android-10.x)**
*   **[Notes for Android 4.4](/web/20201112003349/https://github.com/opengapps/opengapps/wiki/Notes-for-Android-4.4)**
*   **[Notes for Android 5.0](/web/20201112003349/https://github.com/opengapps/opengapps/wiki/Notes-for-Android-5.0)**
*   **[Notes for Android 6.0](/web/20201112003349/https://github.com/opengapps/opengapps/wiki/Notes-for-Android-6.0)**
*   **[Notes for Android 7.x](/web/20201112003349/https://github.com/opengapps/opengapps/wiki/Notes-for-Android-7.x)**
*   **[Notes for Android 8.x](/web/20201112003349/https://github.com/opengapps/opengapps/wiki/Notes-for-Android-8.x)**
*   **[Notes for Android 9.0](/web/20201112003349/https://github.com/opengapps/opengapps/wiki/Notes-for-Android-9.0)**
*   **[Notes for Android 9.x](/web/20201112003349/https://github.com/opengapps/opengapps/wiki/Notes-for-Android-9.x)**
*   **[Notes for Android ARM](/web/20201112003349/https://github.com/opengapps/opengapps/wiki/Notes-for-Android-ARM)**
*   **[Notes for Android x86](/web/20201112003349/https://github.com/opengapps/opengapps/wiki/Notes-for-Android-x86)**
*   **[Notes for CMSetupWizard](/web/20201112003349/https://github.com/opengapps/opengapps/wiki/Notes-for-CMSetupWizard)**
*   **[Package Comparison](/web/20201112003349/https://github.com/opengapps/opengapps/wiki/Package-Comparison)**
*   **[PackageInstallerGoogle](/web/20201112003349/https://github.com/opengapps/opengapps/wiki/PackageInstallerGoogle)**
*   **[Pico Package](/web/20201112003349/https://github.com/opengapps/opengapps/wiki/Pico-Package)**
*   **[Stock Package](/web/20201112003349/https://github.com/opengapps/opengapps/wiki/Stock-Package)**
*   **[Super Package](/web/20201112003349/https://github.com/opengapps/opengapps/wiki/Super-Package)**
*   **[TVStock Package](/web/20201112003349/https://github.com/opengapps/opengapps/wiki/TVStock-Package)**
*   <button type="button" class="f6 mx-auto btn-link muted-link js-wiki-more-pages-link">Show 15 more pages…</button>

</div>

</div>

</div>

<div class="gollum-markdown-content">

<div class="Box Box--condensed mb-4">

<div class="Box-body wiki-custom-sidebar markdown-body">

## [](#home)[Home](Home)

**[Advanced Features and Options](Advanced-Features-and-Options)**  
**[FAQ](FAQ)**  
**[Get Involved](Get-Involved)**  
**[Hotlinking to OpenGApps.org](Hotlinking-to-OpenGApps.org)**

**Packages ([Comparison](Package-Comparison))**

*   [Aroma](Aroma-Package)
*   [Pico](Pico-Package)
*   [Nano](Nano-Package)
*   [Micro](Micro-Package)
*   [Mini](Mini-Package)
*   [Full](Full-Package)
*   [Stock](Stock-Package)
*   [Super](Super-Package)
*   [TVStock](TVStock-Package)

**Configs for**

*   [OnePlus X's OxygenOS](gapps%E2%80%90config-for-OnePlus-X's-OxygenOS)

**Notes for**

*   [Android 4.4](Notes-for-Android-4.4)
*   [Android 5.0](Notes-for-Android-5.0)
*   [Android 6.0](Notes-for-Android-6.0)
*   [Android 7.x](Notes-for-Android-7.x)
*   [Android 8.x](Notes-for-Android-8.x)
*   [Android 9.0](Notes-for-Android-9.0)
*   [Android 10.x](Notes-for-Android-10.x)
*   [Android ARM](Notes-for-Android-ARM)
*   [Android x86](Notes-for-Android-x86)
*   [CMSetupWizard](Notes-for-CMSetupWizard)
*   [PackageInstallerGoogle](PackageInstallerGoogle)

* * *

## [](#links-to-gapps-on-the-play-store)Links to GApps on the Play Store

*   [Google LLC - developer's page](https://web.archive.org/web/20201112003349/https://play.google.com/store/apps/dev?id=5700313618786177705)
*   [Android Auto](https://web.archive.org/web/20201112003349/https://play.google.com/store/apps/details?id=com.google.android.projection.gearhead)
*   [Android Accessibility Suite (Talkback)](https://web.archive.org/web/20201112003349/https://play.google.com/store/apps/details?id=com.google.android.marvin.talkback)
*   [Exchange Services](https://web.archive.org/web/20201112003349/https://play.google.com/store/apps/details?id=com.google.android.gm.exchange)
*   [Carrier Services](https://web.archive.org/web/20201112003349/https://play.google.com/store/apps/details?id=com.google.android.ims)
*   [Gboard (Google Keyboard)](https://web.archive.org/web/20201112003349/https://play.google.com/store/apps/details?id=com.google.android.inputmethod.latin)
*   [Gmail](https://web.archive.org/web/20201112003349/https://play.google.com/store/apps/details?id=com.google.android.gm)
*   [Google Apps Device Policy](https://web.archive.org/web/20201112003349/https://play.google.com/store/apps/details?id=com.google.android.apps.enterprise.dmagent)
*   [Google Calculator](https://web.archive.org/web/20201112003349/https://play.google.com/store/apps/details?id=com.google.android.calculator)
*   [Google Calendar](https://web.archive.org/web/20201112003349/https://play.google.com/store/apps/details?id=com.google.android.calendar)
*   [Google Camera](https://web.archive.org/web/20201112003349/https://play.google.com/store/apps/details?id=com.google.android.GoogleCamera)
*   [Google Chrome](https://web.archive.org/web/20201112003349/https://play.google.com/store/apps/details?id=com.android.chrome)
*   [Google Clock](https://web.archive.org/web/20201112003349/https://play.google.com/store/apps/details?id=com.google.android.deskclock)
*   [Google Cloud Print](https://web.archive.org/web/20201112003349/https://play.google.com/store/apps/details?id=com.google.android.apps.cloudprint)
*   [Google Connectivity Services](https://web.archive.org/web/20201112003349/https://play.google.com/store/apps/details?id=com.google.android.apps.gcs)
*   [Google Contacts](https://web.archive.org/web/20201112003349/https://play.google.com/store/apps/details?id=com.google.android.contacts)
*   [Google Device Health Services](https://web.archive.org/web/20201112003349/https://play.google.com/store/apps/details?id=com.google.android.apps.turbo)
*   [Google Dialer](https://web.archive.org/web/20201112003349/https://play.google.com/store/apps/details?id=com.google.android.dialer)
*   [Google Digital Wellbeing](https://web.archive.org/web/20201112003349/https://play.google.com/store/apps/details?id=com.google.android.apps.wellbeing)
*   [Google Duo](https://web.archive.org/web/20201112003349/https://play.google.com/store/apps/details?id=com.google.android.apps.tachyon)
*   [Google Docs](https://web.archive.org/web/20201112003349/https://play.google.com/store/apps/details?id=com.google.android.apps.docs.editors.docs)
*   [Google Drive](https://web.archive.org/web/20201112003349/https://play.google.com/store/apps/details?id=com.google.android.apps.docs)
*   [Google Earth](https://web.archive.org/web/20201112003349/https://play.google.com/store/apps/details?id=com.google.earth)
*   [Google Fit](https://web.archive.org/web/20201112003349/https://play.google.com/store/apps/details?id=com.google.android.apps.fitness)
*   [Google Indic Keyboard](https://web.archive.org/web/20201112003349/https://play.google.com/store/apps/details?id=com.google.android.apps.inputmethod.hindi)
*   [Google Japanese Input](https://web.archive.org/web/20201112003349/https://play.google.com/store/apps/details?id=com.google.android.inputmethod.japanese)
*   [Google Keep Notes](https://web.archive.org/web/20201112003349/https://play.google.com/store/apps/details?id=com.google.android.keep)
*   [Google Korean Input](https://web.archive.org/web/20201112003349/https://play.google.com/store/apps/details?id=com.google.android.inputmethod.korean)
*   [Google Maps](https://web.archive.org/web/20201112003349/https://play.google.com/store/apps/details?id=com.google.android.apps.maps)
*   [Google Messages](https://web.archive.org/web/20201112003349/https://play.google.com/store/apps/details?id=com.google.android.apps.messaging)
*   [Google News](https://web.archive.org/web/20201112003349/https://play.google.com/store/apps/details?id=com.google.android.apps.magazines)
*   [Google Now Launcher](https://web.archive.org/web/20201112003349/https://play.google.com/store/apps/details?id=com.google.android.launcher)
*   [Google Pay](https://web.archive.org/web/20201112003349/https://play.google.com/store/apps/details?id=com.google.android.apps.walletnfcrel)
*   [Google Photos](https://web.archive.org/web/20201112003349/https://play.google.com/store/apps/details?id=com.google.android.apps.photos)
*   [Google Pinyin Input](https://web.archive.org/web/20201112003349/https://play.google.com/store/apps/details?id=com.google.android.inputmethod.pinyin)
*   [Google Play Books](https://web.archive.org/web/20201112003349/https://play.google.com/store/apps/details?id=com.google.android.apps.books)
*   [Google Play Games](https://web.archive.org/web/20201112003349/https://play.google.com/store/apps/details?id=com.google.android.play.games)
*   [Google Play Movies & TV](https://web.archive.org/web/20201112003349/https://play.google.com/store/apps/details?id=com.google.android.videos)
*   [Google Play Music](https://web.archive.org/web/20201112003349/https://play.google.com/store/apps/details?id=com.google.android.music)
*   [Google Search](https://web.archive.org/web/20201112003349/https://play.google.com/store/apps/details?id=com.google.android.googlequicksearchbox)
*   [Google Sheets](https://web.archive.org/web/20201112003349/https://play.google.com/store/apps/details?id=com.google.android.apps.docs.editors.sheets)
*   [Google Slides](https://web.archive.org/web/20201112003349/https://play.google.com/store/apps/details?id=com.google.android.apps.docs.editors.slides)
*   [Google Sounds](https://web.archive.org/web/20201112003349/https://play.google.com/store/apps/details?id=com.google.android.soundpicker)
*   [Google Street View](https://web.archive.org/web/20201112003349/https://play.google.com/store/apps/details?id=com.google.android.street)
*   [Google Text-to-Speech](https://web.archive.org/web/20201112003349/https://play.google.com/store/apps/details?id=com.google.android.tts)
*   [Google Translate](https://web.archive.org/web/20201112003349/https://play.google.com/store/apps/details?id=com.google.android.apps.translate)
*   [Google VR Services](https://web.archive.org/web/20201112003349/https://play.google.com/store/apps/details?id=com.google.vr.vrcore)
*   [Google Webview Stub](https://web.archive.org/web/20201112003349/https://play.google.com/store/apps/details?id=com.google.android.webview)
*   [Google Webview](https://web.archive.org/web/20201112003349/https://play.google.com/store/apps/details?id=com.google.android.webview)
*   [Google Zhuyin Input](https://web.archive.org/web/20201112003349/https://play.google.com/store/apps/details?id=com.google.android.apps.inputmethod.zhuyin)
*   [Google+](https://web.archive.org/web/20201112003349/https://play.google.com/store/apps/details?id=com.google.android.apps.plus)
*   [Hangouts](https://web.archive.org/web/20201112003349/https://play.google.com/store/apps/details?id=com.google.android.talk)
*   [Pixel Launcher](https://web.archive.org/web/20201112003349/https://play.google.com/store/apps/details?id=com.google.android.apps.nexuslauncher)
*   [Project Fi](https://web.archive.org/web/20201112003349/https://play.google.com/store/apps/details?id=com.google.android.apps.tycho)
*   [Recorder](https://web.archive.org/web/20201112003349/https://play.google.com/store/apps/details?id=com.google.android.apps.recorder)
*   [Wallpapers](https://web.archive.org/web/20201112003349/https://play.google.com/store/apps/details?id=com.google.android.apps.wallpaper)
*   [YouTube](https://web.archive.org/web/20201112003349/https://play.google.com/store/apps/details?id=com.google.android.youtube)

</div>

</div>

</div>

</div>