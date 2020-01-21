Initial PR: [#773](https://github.com/opengapps/opengapps/pull/773).

While making this release, Google has made a lot of changes which affected the development:

1. Now we have `/system_root` in recovery as the main mountpoint instead of `/system`, so we had to adapt mounting scripts to properly detect that.
2. `Pixel Launcher` now requires a system setting to be allowed as the main homescreen app, so in order for it to work, we also had to include an overlay to set it as the default launcher app.
Same applies to the `Digital Wellbeing`, `Actions Services` and `Dialer` apps which have their own overlays now as well.
3. `Pixel Launcher` now requires `Actions Services` since it's using it now as the provider for the user app recommendations.

Apart from that, there are still a few bugs:
- `Photos` FC
- Using `Pixel Launcher` with Q gesture system will result in FC
- [ARM-only] SetupWizard FCs due to Google changing some internal stuff (more details [here](https://forum.xda-developers.com/showpost.php?p=81478751&postcount=6439))

Because of this, we've only enabled `pico` and `nano` build variants in the initial stable release, other variants will be added as soon as the remaining issues are fixed.