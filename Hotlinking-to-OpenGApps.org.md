# Pre-selection
If you are a e.g. a ROM developer and want to hotlink to certain pre-select choices, you can pass some extra parameters to the opengapps.org website. These passed parameters will then be selected by the radio buttons. Fields that are not specified will be set to their default (currently those are: _arm_, _5.1_ and _stock_).

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

## Variant
Setting the package variant is via the ```variant``` variable, valid values are:
* aroma
* stock
* full
* mini
* micro
* nano
* pico

## Example
An example URL with some pre-selections could be:
_http://opengapps.org/?&arch=arm64&api=5.0&variant=aroma_

# Download Hotlink
If you are passing parameters for pre-selection, you can also add an extra parameter to automatically trigger the download of given selection. After loading the website and querying GitHub for the latest available release, the browser will automatically be redirected to the download URL. This can be achieved by passing the ```download``` parameter with the value ```true```.

## Example
An example URL with automatic download of the chosen pre-selection could be:
_http://opengapps.org/?download=true&arch=arm64&api=5.0&variant=aroma_

# Mirroring
Please don't publicly mirror the prebuilt packages without explicit consent of @mfonville, to ensure that users will always be directed to the very latest version and the source code of the project.
With our support for hotlinking, there is no need for outdated mirrors!