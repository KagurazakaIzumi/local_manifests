Local manifests to build AOSP for Xiaomi Mi2.

How to build:
-------------

Initialize repo:

    repo init -u https://android.googlesource.com/platform/manifest -b android-11.0.0_r32
    curl --create-dirs -L -o .repo/local_manifests/local_manifest.xml -O -L https://github.com/KagurazakaIzumi/local_manifests/raw/dev/KagurazakaIzumi/use-tiger-cave-bionic/local_manifest.xml
    repo sync

Compile:

    . build/envsetup.sh
    lunch aosp_aries-userdebug
    make -j otapackage

![](pics/screenshot.png)
