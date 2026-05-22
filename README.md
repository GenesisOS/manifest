![banner](https://raw.githubusercontent.com/GenesisOS/.github/master/profile/BuildBanner.png)

Getting Started
-
### Requirements:
- You have basic knowledge of [Repo](https://source.android.com/source/using-repo.html) and Version Control with [Git](https://source.android.com/source/version-control.html).
- Make sure you have an [Android Build Environment](https://source.android.com/setup/build/initializing) and the [Repo Tool](https://source.android.com/setup/build/downloading) set up.
- 100GB of disk space.

Compiling GenesisOS
-

### First you need to initialize your local repository using the following command:
```
repo init -u https://github.com/GenesisOS/manifest.git -b yume --git-lfs
```
### Then Sync the source code using the following command:
```
repo sync -j$(nproc --all) --force-sync --no-tags --no-clone-bundle --prune --optimized-fetch
```
### Now adapt your Device Trees for GenesisOS and start the build using the following commands:
```
source build/envsetup.sh
lunch genesis_$devicecodename-bp4a-userdebug
mka genesis
```
Now fix the errors during compilation and wait for Successful Build Message. Happy Compiling!

Important Links
-
- [*Join Our Community!*](https://t.me/GenesisOSChat)
- [*Latest GenesisOS Update!*](https://t.me/TheGenesisOS)