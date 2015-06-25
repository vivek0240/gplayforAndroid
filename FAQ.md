COMMON QUESTIONS & ANSWERS (FAQ)
===
####1. I'm having problems that I believe are Open GApps related. What can I do to fix it?
There are 2 things you can do that are almost always guaranteed to fix these types of problems. Please do not post a support request until you have tried these first.
  1. Make certain you are using the **latest version** of [TWRP Recovery](https://twrp.me/) for your device.
    - Other Recovery types are not officially supported
  2. Reinstall your ROM and GApps as part of a 'Clean' install
    - This will remove any data corruption that might be causing your issue

<u>A 'Clean' install consists of the following:</u>
 1. Factory Reset (or manually wipe (format) Data partition - Internal Storage wipe is NOT necessary)
 2. Manually wipe (format) your System partition
 3. Flash your ROM
 4. Flash GApps package
 5. Wipe the Dalvik & cache
 6. Reboot

NOTE: YOU WILL LOSE ALL OF YOUR DATA AND APPLICATION SETTINGS using this method. Be sure to do a nandroid backup prior in case you want to restore later.


####2. I'm having a problem with my Open GApps install. What information do you need to help me?
At a MINIMUM you will need to post your open_gapps_log.txt attached to a XDA Forum post, where the community can try to help you resolve the problem. However, the best method to receive support would be to post your debug logs (open_gapps_debug_logs.tar.gz), using the same method. You will find both of these logs in the same folder as the Open GApps zip file, after the installer has completed.

As with most support forums, the more work you do up front and the more information you provide, the better the feedback you're likely to receive. If you're not willing to put any effort on your end, you'll likely receive nothing from the forum, either.


####3. I'm getting a 'Status Error 6' when I try and install these GApps with CWM. What can I do to fix it?
It likely means you're using CWM v6.0.4.7 Recovery, which is NOT compatible with Open GApps packages.

The problem is due to CWM v6.0.4.7 overwriting the installation script, thereby making it impossible for the installer to do its work. Thankfully, CWM realized the error in doing this and fixed the issue in newer versions. This 'bug' is only found in CWM v6.0.4.7, so even an older version should work, although upgrading your Recovery would be preferable to downgrading.

Also, since CWM is no longer being updated by its original developer (ClockWordMod), it is highly recommended (and required if you want official support) to change to an actively supported Recovery, such as TWRP Recovery


####4. Open GApps install failed with Error Code: XX. What does this code mean?
Error codes have been added to the installer since many users, apparently, don't know how to scroll back through the recovery window and read the actual error message that the installer provided. While there is also a detailed explanation of the error (along with a solution) provided in the log file (open_gapps_log.txt), Error Codes have been added as a final attempt to communicate the error with the user.

Using the information below, you will find a current list of the Error Codes that that install may encounter - along with a recommended solution:
 * `#20` - Incorrect (incompatible) ROM Version: ROM is not compatible with the Open GApps package
Solution: Read your open_gapps_log.txt for details on the incompatibility
 * `#40` - NON-Open GApps Currently Installed: Your device has an incompatible GApps package currently installed
Solution: Read FAQ #7 for an explanation and step by step instructions to fix
 * `#64` - Incompatible device architecture: Your device has been detected as having a different kind of architecture then the package used. Like _arm_ vs _arm64_ vs _x86_ etc. Install the correct Open GApps version for your device.
Solution: Use a compatible version of the Open GApps package for your device's architecture.
 * `#70` - Insufficient Space Available in System Partition: Your device does not have sufficient space available in the system partition to install the Open GApps package
Solution: Read FAQ #6 for a detailed explanation and alternative options

####5. I read that 'Google Camera, Google Keyboard and Google Desk Clock can only be installed during a Clean Install or as an update to an existing Open GApps Installation.' What does this mean?
Experience has shown us that users who install these applications FOR THE FIRST TIME during a 'Clean install' GApps installation almost never have issues or problems with these apps. However, there have been several reports of users experiencing FC's or other strange behavior when they have tried to install these apps later (with GApps), after their device has been set up.

To ensure the best possible user experience, Open GApps will only allow these applications to be installed FOR THE FIRST TIME as part of a 'Clean' install (data wiped) installation. Updates to an existing System (Open GApps) installation will also install fine, plus you can still freely update these apps from the Play Store and have the Open GApps installer update them later with the next Open GApps update.

<u>A 'Clean' install consists of the following:</u>
 1. Factory Reset (or manually wipe (format) Data partition - Internal Storage wipe is NOT necessary)
 2. Manually wipe (format) your System partition
 3. Flash your ROM
 4. Flash GApps package
 5. Wipe the Dalvik & cache
 6. Reboot

NOTE: YOU WILL LOSE ALL OF YOUR DATA AND APPLICATION SETTINGS using this method. Be sure to do a nandroid backup prior in case you want to restore later.

####6. Open GApps install failed with the message 'Insufficient storage space available in System partition'. My device has 16GB (or more) of storage available. How can this be?

Your ROM and GApps are installed in the system partition. The system partition is a separate, fixed-size, stand-alone partition of storage that varies in size by device. ([READ HERE](http://techblogon.com/android-file-system-structure-architecture-layout-details/) for a complete explanation of the Android File System Structure.) While today's newer devices often come with 1.5GB (or more) of storage in the system partition, most devices that are more than a year old have 1GB or less of system storage available. This, coupled with the fact that Google's applications are becoming larger with every update, means that your device may not be able to accommodate our larger GApps packages. 

The reason you won't get this error message with other GApps packages is because Open GApps' installer use a System Partition memory detection system to insure a successful installation and the ability to restore Open GApps after a ROM update. Most other GApps installers do no such checking and leave the responsibility on you to know if your device has sufficient space available. In addition, our installer will generate a detailed log that will show you exactly how the system space on your device is being used. You will find this log (open_gapps_log.txt) in the same folder as the Open GApps zip file, after the installer has completed. Please refer to it for complete details.

You can choose to install a smaller GApps package or you may want to take advantage of Open GApps' [[Advanced Features & Options|Advanced-Features-and-Options]] and remove certain apps you do not use or need (Remember, you can always install these apps later from the Play Store).

####7. I'd like to switch to Open GApps from another GApps provider. What do I need to do?
Open GApps can only be installed on top of an existing Open GApps installation, OR after wiping your system partition. This is to prevent conflicts that could arise from switching GApps packages. If you use the method outlined below, you won't lose any of your data or application settings

In order to switch to Open GApps from another GApps provider you're no longer using, you will need to (from Recovery - **In the order listed**):
 1. Manually wipe (format) your System partition
 2. Flash your ROM
 3. Flash Open GApps package
 4. Wipe the Dalvik & cache
 5. Reboot

NOTE: You won't lose any of your data or application settings using this method. This method MUST be used when switching to Open GApps from another GApps provider.


####8. Can I use Open GApps to update the Google Apps on my Stock ROM?
The short answer is No. Open GApps have always been designed to be installed with custom Android AOSP based ROMs. If you're using a Stock ROM, you should continue to only update your apps through the Google Play Store.

####9. I'm having problems with Google Camera after installing Open GApps Stock. Please fix it!
While Google does say that Google Camera 'Works on phones and tablets running Android 4.4 and up', they clearly didn't intend to include every KitKat or Lollipop ROM on XDA. They likely meant this to include devices running stock or factory versions of Android with proper drivers and kernels. In addition, Photo Sphere and Panorama require a gyro sensor and Photo Sphere, Panorama, and Lens Blur require at least 1 GB RAM. And HDR+ is only available on the Nexus 5 and 6, according to the Play Store description

While even legacy devices are able to run KitKat or Lollipop with a custom ROM, many of these ROM's do not have properly updated KitKat or Lollipop drivers and/or kernels. Instead, they're using modded, patched, or hacked versions of older drivers and kernels. It's likely these situations that lead to problems and/or incompatibilities with Google's camera app. This means that there's NOTHING the Open GApps Team can do to fix this problem for you. Your only likely option is to NOT use the Google Camera on your device or try installing it from the Play Store instead.

####10. Open GApps packages are so big. Will I have any space left over for my stuff after I install?
Open GApps will use LESS of your device's available storage than using a 'bare bones' GApps and downloading the apps from the Play Store. This is because GApps are installed entirely in the System partition, leaving the Data (User) partition for your non-Google apps. Since the System partition is a fixed size, installing GApps here uses storage that would otherwise be left unused (and unavailable for other use).

####11. Why are Open GApps packages so much larger than other GApps packages?
Open GApps are larger than other GApps packages for a couple of reasons:
 * The main reason is that all our GApps packages include the PROPER version of Google Play services for YOUR device. Instead of installing a generic, obsolete, or a potentially improper version, the Open GApps installer detects the hardware dpi of your device and then installs the PROPER version of Google Play services that was intended for your device. This means that the Open GApps packages must include multiple versions, which significantly increases the size of the packages.
 * Open GApps Stock version includes all of the Google Apps that come by default on a Google Nexus device. Since our intention is to enhance the Google Android experience, we don't think it makes sense to limit the apps included in this Open GApps package.

####12. Is it necessary to reinstall Open GApps EVERY time I update my ROM?
Probably not. If your ROM supports addon.d backup functionality (most ROM's do), it's not necessary to install Open GApps with each ROM update - as long as you don't manually wipe the System partition. The backup script will backup your installed GApps and restores them after your ROM has been updated. However, it is a good idea to install an updated GApps from time to time as functionality may be added or improvements made.

####13. What if an app is updated in the Play Store? Should I install the update or wait for a GApps update?
Go ahead and install the update. The next time you update Open GApps, Android automatically will remove the app you installed from the Play Store if the Open GApps' version is the same or newer than the version you installed from the Play Store. Just be certain to wipe Dalvik and cache after flashing the updated GApps.

####14. Can I install an updated Open GApps package without updating my ROM?
Certainly! Simply install the Open GApps package directly from Recovery and wipe Dalvik and cache after flashing the updated GApps.

####15. How come you don't include {MyFavoriteApp} in Open GApps?
For an application to be included in Open GApps, it has to meet the following criteria:
 * It must be a Google App (GApps = Google Apps.)
 * To be included in the 'Stock' package it must be an application that comes by default Google Nexus devices.
 * It must be a globally used app (not language or country specific)

####16. I found a newer version of {MyFavoriteApp} on APKMirror.com. How come you didn't include it in the latest GApps?
Just because an apk is uploaded to APKMirror or has an article written on Android Police, doesn't mean it will automatically be included in Open GApps. Only apps that can be verified that Google has intended for public release will be included. The primary method used to determine the latest version of an app is the Google Play Store date, which HAS ALWAYS listed the date of the most recent public release for the most current version of Android. So, if you find an updated apk on APKMirror and don't see it included in Open GApps, it's likely a leak or preview version. Of course, you're always free to sideload the leaks and previews on your own, should you desire.

####17. There are a couple of apps I never use. Can I uninstall them?
Using the Advanced Features & Options, you can actually bypass the installation or remove any GApps installed application from your device. You could also choose to freeze / disable the app. This will prevent the app from using valuable system resources and leaves the unused app lying dormant in the System partition where it's not using any of your available storage. Plus, the app will remain disabled even after you update GApps.

####18. How do I Freeze / Disable an app?
By going to Settings > Apps > {scroll to ALL} > {select app} > Disable.

####19. Can I use Titanium Backup to integrate GApps updates into the ROM?
It is NOT recommended to use Titanium Backup to integrate GApps updates into the ROM. The reason is, using Titanium Backup to integrate GApps updates is going to be hit or miss, at best. That's because Titanium Backup does not integrate the supporting libraries (*.so files). Therefore, if an application update includes updated libraries, the integration will fail or fail to offer complete functionality. The reason it "seems" to work sometimes is that supporting libraries are often not updated when the application is updated. In those cases, the integration will work fine because the older libraries are the correct ones. If an application doesn't have supporting libraries then Titanium Backup integration works fine. However, our recommendation is to NOT use Integration.