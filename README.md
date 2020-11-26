# KangOS : 
<centre> Yet Another cherry-picked Custom ROM <centre/>

<img src="https://github.com/sherifrahim/android_manifest/blob/eleven/banner.png?raw=true">

Credits:
=======
 * [**AOKP**](https://github.com/AOKP)[AOKP The Original Masters of Kang]
 * [**RevengeOS**](https://github.com/RevengeOS)
 * [**AOSP**](https://android.googlesource.com)
 * [**LineageOS**](https://github.com/LineageOS)
 * [**DirtyUnicorns**](https://github.com/dirtyunicorns)
 * [**PixelExperience**](https://github.com/PixelExperience)
 * [**ABC**](https://github.com/ezio84?tab=repositories)
 * [**Project-Awaken**](https://github.com/Project-Awaken)
 * [**POSP**](https://github.com/PotatoProject)
 * [**Project-Streak**](https://github.com/ProjectStreak)

-----------------------------------------------------------------------------


Getting Started:
==============

To get started with the building process, you'll need to get familiar with [Git and Repo](http://source.android.com/source/using-repo.html).

To initialize your local repository, use a command like this:

```bash
repo init -u https://github.com/Kang-OS-R/android_manifest -b eleven
```
Then to sync up:
================

```bash
repo sync -c --force-sync --no-tags --no-clone-bundle -j$(nproc --all) --optimized-fetch --prune
```

KangOS FlAGS :
================
- USE_GAPPS := true, use this flag to make GApps Build.

- Screen-Off FOD, FOD Animation and Icon Picker support is there in ROM Source, just add appropriate strings in your device tree to enable them.

Finally to build:
====================

From root directory of Project, perform following commands in terminal


```bash
source build/envsetup.sh
lunch kangos_<devicecodename>-userdebug
make bacon
```
-----------------------------------------------------------------------------
After Succesfully Compiling KangOS for your device, dont forgot to take a look at this : 

>> To get official maintainership for KangOS, refer [**here**](https://telegra.ph/Apply-for-KANG-OS-Official-11-26).

>> Contact us via   <a href="https://t.me/kangos">
<img src="https://img.shields.io/badge/Telegram-Chat-blue?style=for-the-badge">


