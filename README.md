## TWRP device tree for Galaxy Tab A 10.1 LTE (2016) with S-Pen

Add to `.repo/local_manifests/gtanotexllte.xml`:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<manifest>
	<project path="device/samsung/gtanotexllte" name="android_device_samsung_gtanotexllte" remote="TeamWin" revision="android-6.0" />
</manifest>
```

Then run `repo sync` to check it out.

To build:

```sh
. build/envsetup.sh
lunch omni_gtanotexllte-eng
make -j5 recoveryimage
```

Kernel sources are available at: https://github.com/jcadduono/android_kernel_samsung_exynos7870/tree/twrp-6.0
