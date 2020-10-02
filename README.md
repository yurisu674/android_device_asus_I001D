# Device Tree Asus ROG Phone II (ASUS_I001D)

The Asus ROG Phone II (codenamed _"ASUS_I001D"_) is a smartphone from Asus.
It was released in September 2019.

## Compile

First download minimal AOSP android-11 tree:

```
repo init -u git://github.com/minimal-manifest-twrp/platform_manifest_twrp_aosp.git -b twrp-11
```
Then add this project to a new local manifest (.repo/local_manifests/<your-file-name.xml>:

```xml
<project name="android_device_asus_I001D" path="device/asus/I001D" remote="TeamWin" revision="android-11" />
```

Now you can sync your source:

```
repo sync
```

Finally execute these:

```
. build/envsetup.sh
lunch omni_I001D-eng
mka bootimage
```

To test it:

```
fastboot boot $OUT/boot.img
```