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
repo init -u https://github.com/GenesisOS/manifest.git -b verve-qpr2 --git-lfs
```
### Then Sync the source code using the following command:
```
repo sync -j$(nproc --all) --force-sync --no-tags --no-clone-bundle --prune --optimized-fetch
```
### Generating Keys
Signing the builds is a must to pass Device Integrity and CTS on the Builds. To generate keys for signing the builds run the following command in the root directory of the ROM:
```
subject='/C=US/ST=State/L=City/O=Android/OU=Android/CN=Android/emailAddress=email@example.com'
for x in releasekey platform shared media networkstack verity otakey testkey sdk_sandbox bluetooth nfc; do \
    ./development/tools/make_key vendor/genesis/signing/keys/$x "$subject"; \
done
```
### Now adapt your Device Trees for GenesisOS and start the build using the following commands:
```
source build/envsetup.sh
breakfast devicecodename
mka genesis
```
Now fix the errors during compilation and wait for Successful Build Message. Happy Compiling!

Important Links
-
- [*Join Our Community!*](https://t.me/GenesisOSChat)
- [*Latest GenesisOS Update!*](https://t.me/TheGenesisOS)