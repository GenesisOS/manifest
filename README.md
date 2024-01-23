## Getting source code

First, make sure you have an [Android build environment](https://source.android.com/setup/build/initializing) and the [repo tool](https://source.android.com/setup/build/downloading) set up. After that, run the following commands:

```
repo init -u https://github.com/GenesisOS/manifest.git -b utopia --git-lfs
```

```
repo sync -j$(nproc --all) --force-sync --no-tags --no-clone-bundle --prune --optimized-fetch
```

```
source build/envsetup.sh
lunch genesis_device-buildtype
mka genesis
```

This is a large download that will take approximately 100 GB of disk space, so plan accordingly.

Good luck!
