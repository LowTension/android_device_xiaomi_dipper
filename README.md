# android_device_xiaomi_dipper
Device tree for build TWRP for Xiaomi MI 8(dipper) only.

## Downloading TWRP sources
```
repo init -u git://github.com/minimal-manifest-twrp/platform_manifest_twrp_omni.git -b twrp-10.0
repo sync
```
### Add this to .repo/manifest.xml
```xml
<project path="device/xiaomi/dipper" name="ZonaRMR/android_device_xiaomi_dipper" remote="github" revision="android-10.0" />
<project name="TeamWin/android_device_qcom_twrp-common" path="device/qcom/common" remote="github" revision="android-10"/>
```

## Compile TWRP

```
. build/envsetup.sh
lunch omni_dipper-eng
mka recoveryimage
```

## Thanks to  
althafvly@xda for the device tree base
