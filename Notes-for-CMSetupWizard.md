If you use the `CMSetupWizard` keyword to remove Cyanogenmod's Setupwizard, but not have set-up your device yet, you will be hit by the issue that the pull-down Quick Settings menu doesn't work anymore (See [CM bug #2889](https://jira.cyanogenmod.org/browse/NIGHTLIES-2889)).

This issue exists because Cyanogenmod decided (see [CM bug #2431](http://review.cyanogenmod.org/#/q/topic:CYNGNOS-2431)) that the Quick Settings should only be shown if their own provision database key `CM_SETUP_WIZARD_COMPLETED` has been set, instead of sticking to Google's and AOSP's key `DEVICE_PROVISIONED`.
Google's setupwizard obviously does not set CM's key, thus you **need the Cyanogenmod setupwizard**.

So either you need to keep CMSetupWizard installed for at least the first boot, or you need to apply a manual workaround, or you need to patch the ROM

#### Workarounds _(requires root)_
* The following may be executed from a command prompt in booted Android, and is only necessary once:

    `su -c 'settings --cm put secure cm_setup_wizard_completed 1'`


#### Patch
*TODO*

***
#### References
* [Discussion about not making CMSetupwizard removed by Open GApps default anymore](https://github.com/opengapps/opengapps/commit/ca0704182ac3c9f47d1ad4c5494500866ba42665)