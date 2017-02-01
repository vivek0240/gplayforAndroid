If you use the `CMSetupWizard` keyword to remove CyanogenMod's SetupWizard, but not have set-up your device yet, you will be hit by the issue that the pull-down Quick Settings menu doesn't work anymore (See [CM bug #2889](https://jira.cyanogenmod.org/browse/NIGHTLIES-2889)).

This issue exists because CyanogenMod decided (see [CM bug #2431](http://review.cyanogenmod.org/#/q/topic:CYNGNOS-2431)) that the Quick Settings should only be shown if their own provision database key `CM_SETUP_WIZARD_COMPLETED` has been set, instead of sticking to Google's and AOSP's key `DEVICE_PROVISIONED`.
Google's SetupWizard obviously does not set CM's key, thus you **'need' the CyanogenMod SetupWizard**.

So either you need to keep CMSetupWizard installed for at least the first boot, or you need to apply a manual workaround, or you need to patch the ROM.

#### Affected ROMs
CyanogenMod 13 and LineageOS 13 or those based on them (the CM14+ codebase used Google's new Quick Settings code, resolving it).

#### Workarounds _(requires root)_
* The following may be executed from a command prompt in booted Android, and is only necessary once:

    `su -c 'settings --cm put secure cm_setup_wizard_completed 1'`

* Flash the **_CMSetup Fix for GApps_ Installer** zip by [osm0sis](https://github.com/osm0sis) via custom recovery to install a _su.d script_ that will automatically execute the above command at the appropriate time following first boot. It is available in his xda-developers [Odds and Ends](http://forum.xda-developers.com/showthread.php?t=2239421) thread.

#### Patch
*TODO*

***
#### References
* [Discussion about not making CMSetupWizard removed by Open GApps default anymore](https://github.com/opengapps/opengapps/commit/ca0704182ac3c9f47d1ad4c5494500866ba42665)
* ["Odds and Ends" thread post detailing the technical difficulties related to the CMSetupWizard fix](https://forum.xda-developers.com/showpost.php?p=67444950&postcount=721)
