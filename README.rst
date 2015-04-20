=======
CVDrone
=======

A modified FreeFlight2 application that includes code to access video stream
using OpenCV

Installation
============

1) Install Android SDK and NDK
------------------------------

Note that you need the x86 version of the NDK (the ARDroneLib FFMPEG makefile has hardcoded
paths that expect a x86 NDK)

- download Android SDK base package:
http://developer.android.com/sdk/index.html
- untar SDK in $HOME/dev/sdk (or any other location)
- export PATH=${PATH}:$HOME/android/android-sdk-linux_x86/tools
- apt-get install ant
- run 'android'
  * download SDK 2.2
- download Android NDK r5b package:
- untar NDK to $HOME/dev/sdk (or any other location)

2) Install OpenCV4Android
-------------------------
http://docs.opencv.org/doc/tutorials/introduction/android_binary_package/O4A_SDK.html#o4a-sdk

3) Build application
--------------------
- Move to 'adfreeflight' app folder.
- Copy environment.properties.example to environment.properties
- Edit environment.properties and set paths to NDK and ARDroneLib.
- Update file local.properties with correct path to SDK.
- Run './build.sh release', './build.sh debug' or './build.sh clean' in order to make debug version, release version or clean.
- AdFreeFlight-release.apk or AdFreeFlight-debug.apk should appear under <project>/bin directory.

4) Install application on Android phone
---------------------------------------
  * connect phone via USB
  * adb install -r <project>/bin/AdFreeFlight-release.apk
