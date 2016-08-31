## Flash Instructions
Flash Open GApps **directly** after flashing your ROM and do **not** boot your device in between.

For 6.0 the GoogleTTS is part of all the packages, because SetupWizard demands TTS, and some 6.0 ROMs don't have any AOSP TTS included. If you use a [[gapps-config|Advanced-Features-and-Options#the-gapps-config-file]] file make sure to include it in your installation or ask your ROM developer to include AOSP TTS.

## Permissions patch for ROM Devs
If you still experience Force Closures of the Setup Wizard at first boot or Google Play Services your ROM could benefit from [this patch](https://github.com/TeamExodus/frameworks_base/commit/9c36be651e83fb039a262682839bd920b033007a) by @TheCrazyLex
It grants the necessary permissions to GApps explicitly, even when their Stock/AOSP counterparts are still installed.

This patch is included by default in most ROMs, but not in AOSP.

***
## Workaround for advanced users
_!Warning no official support provided for this method!_

You can also try to manually workaround using several adb commands and a script:

Put the following contents in a file named `fix_open_gapps_permissions.sh`
```shell
#!/system/bin/env bash

# taken from https://github.com/TeamExodus/frameworks_base/commit/9c36be651e83fb039a262682839bd920b033007a
# converted to bash script by @jomo

PHONE_PERMISSIONS="READ_PHONE_STATE CALL_PHONE READ_CALL_LOG WRITE_CALL_LOG ADD_VOICEMAIL USE_SIP PROCESS_OUTGOING_CALLS"
CONTACTS_PERMISSIONS="READ_CONTACTS WRITE_CONTACTS GET_ACCOUNTS"
LOCATION_PERMISSIONS="ACCESS_FINE_LOCATION ACCESS_COARSE_LOCATION"
CALENDAR_PERMISSIONS="READ_CALENDAR WRITE_CALENDAR"
SMS_PERMISSIONS="SEND_SMS RECEIVE_SMS READ_SMS RECEIVE_WAP_PUSH RECEIVE_MMS READ_CELL_BROADCASTS"
MICROPHONE_PERMISSIONS="RECORD_AUDIO"
CAMERA_PERMISSIONS="CAMERA"
SENSORS_PERMISSIONS="BODY_SENSORS"
STORAGE_PERMISSIONS="READ_EXTERNAL_STORAGE WRITE_EXTERNAL_STORAGE"

grantPerms() {
  for perm in $2; do
    echo ">" pm grant "$1" android.permission."$perm"
    pm grant "$1" android.permission."$perm" 2>/dev/null
  done
}

# Google Account
googleaccountPackage="com.google.android.gsf.login"
grantPerms "$googleaccountPackage" "$CONTACTS_PERMISSIONS"
grantPerms "$googleaccountPackage" "$PHONE_PERMISSIONS"

# Google App
googleappPackage="com.google.android.googlequicksearchbox"
grantPerms "$googleappPackage" "$CALENDAR_PERMISSIONS"
grantPerms "$googleappPackage" "$CAMERA_PERMISSIONS"
grantPerms "$googleappPackage" "$CONTACTS_PERMISSIONS"
grantPerms "$googleappPackage" "$LOCATION_PERMISSIONS"
grantPerms "$googleappPackage" "$MICROPHONE_PERMISSIONS"
grantPerms "$googleappPackage" "$PHONE_PERMISSIONS"
grantPerms "$googleappPackage" "$SMS_PERMISSIONS"
grantPerms "$googleappPackage" "$STORAGE_PERMISSIONS"

# Google Play Services
gmscorePackage="com.google.android.gms"
grantPerms "$gmscorePackage" "$SENSORS_PERMISSIONS"
grantPerms "$gmscorePackage" "$CALENDAR_PERMISSIONS"
grantPerms "$gmscorePackage" "$CAMERA_PERMISSIONS"
grantPerms "$gmscorePackage" "$CONTACTS_PERMISSIONS"
grantPerms "$gmscorePackage" "$LOCATION_PERMISSIONS"
grantPerms "$gmscorePackage" "$MICROPHONE_PERMISSIONS"
grantPerms "$gmscorePackage" "$PHONE_PERMISSIONS"
grantPerms "$gmscorePackage" "$SMS_PERMISSIONS"
grantPerms "$gmscorePackage" "$STORAGE_PERMISSIONS"

# Google Connectivity Services
gcsPackage="com.google.android.apps.gcs"
grantPerms "$gcsPackage" "$CONTACTS_PERMISSIONS"
grantPerms "$gcsPackage" "$LOCATION_PERMISSIONS"

# Google Contacts Sync
googlecontactssyncPackage="com.google.android.syncadapters.contacts"
grantPerms "$googlecontactssyncPackage" "$CONTACTS_PERMISSIONS"

# Google Backup Transport
googlebackuptransportPackage="com.google.android.backuptransport"
grantPerms "$googlebackuptransportPackage" "$CONTACTS_PERMISSIONS"

# Google Play Framework
gsfcorePackage="com.google.android.gsf"
grantPerms "$gsfcorePackage" "$CONTACTS_PERMISSIONS"
grantPerms "$gsfcorePackage" "$PHONE_PERMISSIONS"

# Google Setup Wizard
setupwizardPackage="com.google.android.setupwizard"
grantPerms "$setupwizardPackage" "$CONTACTS_PERMISSIONS"
grantPerms "$setupwizardPackage" "$PHONE_PERMISSIONS"

# Google Play Store
vendingPackage="com.android.vending"
grantPerms "$vendingPackage" "$CONTACTS_PERMISSIONS"
grantPerms "$vendingPackage" "$PHONE_PERMISSIONS"
grantPerms "$vendingPackage" "$LOCATION_PERMISSIONS"
grantPerms "$vendingPackage" "$SMS_PERMISSIONS"
```

The following commands will copy this script to your device and execute it, you should do this *after Android has booted*, you may delete the file afterwards.
```shell
adb push fix_open_gapps_permissions.sh /sdcard/
adb shell 'bash /sdcard/fix_open_gapps_permissions.sh'
adb shell 'rm /sdcard/fix_open_gapps_permissions.sh'
```
