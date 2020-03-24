Initial PR: [#773](https://github.com/opengapps/opengapps/pull/773).

While making this release, Google has made a lot of changes which affected the development:

1. Google has removed the `Trusted Face` feature for security reasons (see [this post](https://www.androidpolice.com/2019/09/04/trusted-face-smart-unlock-method-has-been-removed-from-android-devices/)). We've removed the corresponding code for the `FaceDetect` and `FaceUnlock` for all platforms.
2. Now we have `/system_root` in recovery as the main mountpoint instead of `/system`, so we had to adapt mounting scripts to properly detect that.
3. `Pixel Launcher` now requires a system setting to be allowed as the main homescreen app, so in order for it to work, we also had to include an overlay to set it as the default launcher app.
Same applies to the `Digital Wellbeing`, `Actions Services` and `Dialer` apps which have their own overlays now as well.
4. `Pixel Launcher` now requires `Actions Services` since it's using it now as the provider for the user app recommendations.
5. `Webview` implementation changed again in Q - see [this article](https://www.xda-developers.com/google-chrome-no-longer-webview-provider-android-10/). Because of this, now we additionally ship the `TrichromeLibrary` which **has to match** the versions of the `Chrome` and `Webview` apps.
For now this is **ARM64-only**, but once we find an implementation for this for ARM packages, this will be added there as well.

Apart from that, there are still a few bugs:
- `Photos` FC
- ~Using `Pixel Launcher` with Q gesture system will result in FC~ fixed now

Because of this, we've only enabled build variants up to the `micro` in the current stable release, other variants will be added as soon as the remaining issues are fixed.