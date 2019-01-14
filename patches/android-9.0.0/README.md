# Wifi-Display Patch for Android 9
## Patch Info
AOSP Project:
https://android.googlesource.com/platform/frameworks/av/

Parent Commit:
59a2058610bb56c26120e256c0cf4198af1d901d android-9.0.0_r20

Changes:
1. Reverted: stagefright: remove Miracast sender code.
 https://android.googlesource.com/platform/frameworks/av/+/d0a98fa05f0f6719b93d000c4638230af06e0b99
2. Reverted: Removed unused class and its test.
 https://android.googlesource.com/platform/frameworks/av/+/e885915204f252c93a072ba1a8802f5811e40b3d
3. fix build errors.
4. fix graphics buffer handle not match.
5. add patches in audioflinger to allow capture audio output.

## Prepare for AOSP build
https://source.android.com/setup/build/initializing  
https://source.android.com/setup/build/downloading  
https://source.android.com/setup/build/building

## Apply wifi-display patch
```bash
cd frameworks/av/
git apply wifi-display.patch
```

## Build modules for wifi display
```bash
source build/envsetup.sh
lunch aosp_sailfish-userdebug
make libmediaplayerservice libwilhelm libandroid_runtime libmedia libaudioflinger libserviceutility libstagefright libstagefright_wfd -j4
```

## Replace files
```
system/lib/libaudioflinger.so
system/lib64/libaudioflinger.so
system/lib/libserviceutility.so
system/lib64/libserviceutility.so
system/lib/libmedia.so
system/lib64/libmedia.so
system/lib/libwilhelm.so
system/lib64/libwilhelm.so
system/lib/libandroid_runtime.so
system/lib64/libandroid_runtime.so
system/lib/libstagefright.so
system/lib64/libstagefright.so
system/lib/libstagefright_wfd.so
system/lib64/libstagefright_wfd.so
system/lib/libmediaplayerservice.so
```
