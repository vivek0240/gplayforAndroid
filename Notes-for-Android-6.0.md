To install Open GApps on 6.0 your ROM needs the following patch to prevent Force Closures at first boot: https://github.com/TeamExodus/frameworks_base/commit/9c36be651e83fb039a262682839bd920b033007a

This patch is included by default in most ROMs, but not in AOSP.

You need to flash Open GApps **directly** after flashing your ROM and **not** boot your device in between.

For 6.0 the GoogleTTS is part of all the packages, because SetupWizard seems to demand this in some situations. If you use a [[gapps-config|Advanced-Features-and-Options#the-gapps-config-file]] file make sure to include it in your installation!