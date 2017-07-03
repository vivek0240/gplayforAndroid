If you use the `CMSetupWizard` keyword to remove CyanogenMod's SetupWizard, but you have not set-up your device yet, you will be hit an issue that causes the Quick Settings menu to stop working. (See [CM bug #2889](https://jira.cyanogenmod.org/browse/NIGHTLIES-2889)).

This issue exists because CyanogenMod decided (see [CM bug #2431](http://review.cyanogenmod.org/#/q/topic:CYNGNOS-2431)) that the Quick Settings should only be enabled if their own provision database key `CM_SETUP_WIZARD_COMPLETED` has been set, instead of sticking to Google's and AOSP's key `DEVICE_PROVISIONED`.
Google's SetupWizard obviously does not set CM's key, thus you **'need' the CyanogenMod SetupWizard**.

So you either need to keep CMSetupWizard installed for at least the first boot, apply a manual workaround or patch the ROM.

#### Affected ROMs
CyanogenMod 13, LineageOS 13 and those based on them (the CM14+ codebase uses Google's new Quick Settings code, resolving the issue).

#### Workarounds _(requires root)_
* The following command may be executed from a terminal in booted Android, and is only necessary once:

    `su -c 'settings --cm put secure cm_setup_wizard_completed 1'`

* Flash the **_CMSetup Fix for GApps_ Installer** zip by [osm0sis](https://github.com/osm0sis) via a custom recovery to install a _su.d script_ that will automatically execute the above command at the appropriate time following first boot. It is available in his xda-developers [Odds and Ends](http://forum.xda-developers.com/showthread.php?t=2239421) thread.

#### Patch
*TODO*

As for now LineageOS removed this in favor of USER_SETUP_COMPLETE

https://review.lineageos.org/#/q/branch:cm-14.1+CM_SETUP_WIZARD_COMPLETED

It's unclear whether this will be tied to and thus breaking any features going forward.

***
#### References
* [Discussion about making CMSetupWizard bot being removed by Open GApps default anymore](https://github.com/opengapps/opengapps/commit/ca0704182ac3c9f47d1ad4c5494500866ba42665)
* ["Odds and Ends" thread post detailing the technical difficulties related to the CMSetupWizard fix](https://forum.xda-developers.com/showpost.php?p=67444950&postcount=721)
