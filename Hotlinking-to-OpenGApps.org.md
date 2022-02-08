# Pre-selection
If you are an e.g. a ROM developer and want to hotlink to certain pre-select choices, you can pass some extra parameters to the opengapps.org website. These passed parameters will then be selected by the radio buttons. Fields that are not specified will be set to their default (currently those are: _arm64_, _10.0_, and _stock_).

## Platform
Setting the platform architecture is via the ```arch``` variable, valid values are:
* arm
* arm64
* x86
* x86_64

## Android
Setting the android version is via the ```api``` variable, valid values are:
* 4.4
* 5.0
* 5.1
* 6.0
* 7.0
* 7.1
* 8.0
* 8.1
* 9.0
* 10.0
* 11.0

## Variant
Setting the package variant is via the ```variant``` variable, valid values are:
* aroma
* super
* stock
* full
* mini
* micro
* nano
* pico
* tvstock

## Example
An example URL with some pre-selections could be:
_https://opengapps.org/?arch=arm64&api=10.0&variant=aroma_

# Download Hotlink
If you are passing parameters for pre-selection, you can also add an extra parameter to automatically trigger the download of given selection. After loading the website and querying GitHub for the latest available release, the browser will automatically be redirected to the download URL. This can be achieved by passing the ```download``` parameter with the value ```true```.

## Example
An example URL with automatic download of the chosen pre-selection could be:
_https://opengapps.org/?download=true&arch=arm64&api=10.0&variant=aroma_

# Mirroring
Please don't publicly mirror the prebuilt packages without the explicit consent of @mfonville, to ensure that users will always be directed to the very latest version and the source code of the project.
For more information see our [blog article about the no-mirror policy](https://opengapps.org/blog/post/2016/03/18/the-no-mirror-policy/)

With hotlinking support provided by [OpenGApps.org](https://opengapps.org), there is no need for outdated mirrors!