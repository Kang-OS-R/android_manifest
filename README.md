# KangOS #

<img src="https://i.ibb.co/Bg47twC/Pics-Art-10-11-01-40-57.jpg"> 

Credits:
=======
 * [**AOKP**](https://github.com/AOKP)[AOKP The Original Masters of Kang]
 * [**RevengeOS**](https://github.com/RevengeOS)
 * [**AOSP**](https://android.googlesource.com)
 * [**LineageOS**](https://github.com/LineageOS)
 * [**DirtyUnicorns**](https://github.com/dirtyunicorns)
 * [**AospExtended**](https://github.com/AospExtended)
 * [**PixelExperience**](https://github.com/PixelExperience)
 * [**ABC**](https://github.com/ezio84?tab=repositories)

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

Finally to build:
====================

From root directory of Project, perform following commands in terminal


```bash
source build/envsetup.sh
lunch kangos_<devicecodename>-userdebug
make bacon
```
-----------------------------------------------------------------------------

