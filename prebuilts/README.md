# Prebuilt binaries for Android 9 Wifi-Display

## Devices
* sailfish   - Pixel
* marlin     - Pixel XL
* walleye    - Pixel 2
* taimen     - Pixel 2 XL
* blueline   - Pixel 3
* crosshatch - Pixel 3 XL

## Base Images
https://developers.google.com/android/images

## Change build.prop
Add this line to build.prop:
```
persist.debug.wfd.enable=1
```

## adb push
```bash
adb push system/lib/libaudioflinger.so /system/system/lib/libaudioflinger.so
adb push system/lib64/libaudioflinger.so /system/system/lib64/libaudioflinger.so
adb push system/lib/libserviceutility.so /system/system/lib/libserviceutility.so
adb push system/lib64/libserviceutility.so /system/system/lib64/libserviceutility.so
adb push system/lib/libmedia.so /system/system/lib/libmedia.so
adb push system/lib64/libmedia.so /system/system/lib64/libmedia.so
adb push system/lib/libwilhelm.so /system/system/lib/libwilhelm.so
adb push system/lib64/libwilhelm.so /system/system/lib64/libwilhelm.so
adb push system/lib/libandroid_runtime.so /system/system/lib/libandroid_runtime.so
adb push system/lib64/libandroid_runtime.so /system/system/lib64/libandroid_runtime.so
adb push system/lib/libstagefright.so /system/system/lib/libstagefright.so
adb push system/lib64/libstagefright.so /system/system/lib64/libstagefright.so
adb push system/lib/libstagefright_wfd.so /system/system/lib/libstagefright_wfd.so
adb push system/lib64/libstagefright_wfd.so /system/system/lib64/libstagefright_wfd.so
adb push system/lib/libmediaplayerservice.so /system/system/lib/libmediaplayerservice.so
```
