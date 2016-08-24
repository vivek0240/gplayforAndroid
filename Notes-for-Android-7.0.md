# APK Signature Scheme v2
Very probably the new [APK Signature Scheme v2](https://source.android.com/security/apksigning/v2.html) will give problems for any GApps package on Android Nougat.

If a Google app receives an update from the Play Store, the libraries in its APK are usually compressed. But the libraries need to be stored in a decompressed manner within the APK to make them install-able on the `/system` partition. This results in Open GApps having to re-package the APK which changes its *outside*. This did not intervene with the original signature scheme (that only verified the *inside* of the APK), but does not pass the v2 scheme's check anymore.

Failing to pass the v2 scheme is only fatal if `X-Android-APK-Signed: 2` is included in the `META-INF/*.SF` files. But unfortunately this header is included in Google's most recent apps.
This implies that the ROM needs a patch to allow APKs on `/system` to fail the v2 test even if the `X-Android-APK-Signed: 2` header is present and only check the v1 signature.