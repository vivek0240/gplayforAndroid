The main purpose of this specific gapps-config for OnePlus X's OxygenOS is to remove the stock GApps and reinstall them using Open GApps packages (stock or higher) and also to offer you the chance to install only that GApps that you want.

You personalize this gapps-config to meet your demands. To do so please read [Advanced Features and Options](https://github.com/opengapps/opengapps/wiki/Advanced-Features-and-Options).

This gapps-config is organized in 2 steps:

**\#1** - Remove stock GApps

**\#2** - Install Open GApps (the exact same apps to replicate the stock installation)

I highly suggest to don't remove any keywords from step #1. If you remove any of that, after installation may occur apk conflicts.

At step #2 you can remove the keywords corresponding to which GApps you don't want to install, or even add more keywords. The keywords tagged with _#Safe to remove_ are indeed safe to be removed(they are not essential apps). An example of essential app is Google Play Music app, it is essential because it is the only music player included as default in OxygenOS. Of course you can add, remove, replace any keyword to meet your demands .

_gapps-config.txt_
```
#ATENTION! This script is specific for OnePlus X's OxygenOS.
#You are using this script on your own risk!
#Requires Open GApps stock package or higher! Download it from here: http://opengapps.org/?arch=arm&api=5.1&variant=stock

#Read more about gapps-config file here: https://github.com/opengapps/opengapps/wiki/Advanced-Features-and-Options

#1
#Remove stock GApps
#/system/app
(Bugle)
(CalendarGoogle)
(Chrome)
(ConfigUpdater)
(DeskClockGoogle)
(Drive)
(DMAgent)
(EditorsDocs)
(EditorsSheets)
(EditorsSlides)
(FaceLock)
(Gmail2)
(GmailExchange)
(GoogleContactsSyncAdapter)
(GoogleTTS)
(Hangouts)
(Keep)
(LatinImeGoogle)
(Maps)
(Music2)
(Photos)
(PlayGames)
(PlusOne)
(talkback)
(WebViewGoogle)
(Videos)
(YouTube)

#/system/priv-app
(GmsCore)
(GoogleBackupTransport)
(GoogleFeedback)
(GoogleLoginService)
(GoogleOneTimeInitializer)
(GooglePartnerSetup)
(GoogleServicesFramework)
(Phonesky)
(Velvet)
(SetupWizard)

#2
include
#Install GApps
CalendarGoogle
Chrome
ClockGoogle
DMAgent #Safe to remove
Docs #Safe to remove
Drive #Safe to remove
ExchangeGoogle
FaceDetect
FaceUnlock
Gmail
GooglePlus #Safe to remove
GoogleTTS
Hangouts #Safe to remove
Keep #Safe to remove
KeyboardGoogle #Safe to remove(if you have Swiftkey installed)
Maps
Messenger
Movies #Safe to remove
Music
Photos
PlayGames
Sheets #Safe to remove
Slides #Safe to remove
Search
Talkback
WebviewGoogle
YouTube
```

**IMPORTANT**

**!**This script **requires** at least the **stock package**! If you will use smaller packages you will have missing gapps!

**!**Before flash you may want to backup your system partition in case that something goes wrong.
I tested the config myself and it works as it should.

**!**This gapps-config was written specifically for OPX's OxygenOS to remove the stock gapps and reinstall them. On AOSP based ROMs you won't need this specific gapps-config!

**Download:**

[Open GApps arm 5.1 stock package](http://opengapps.org/?arch=arm&api=5.1&variant=stock)

[gapps-config.txt](https://www.androidfilehost.com/?fid=24269982087021492)