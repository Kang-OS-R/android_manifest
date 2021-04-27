# KangOS

<centre> Yet Another cherry-picked [AOSP](https://source.android.com/) Custom ROM <centre/>


![IMG_20210414_110617_741](https://user-images.githubusercontent.com/66476963/114659794-d9dbd600-9d11-11eb-90c9-c17fea4c399b.jpg)

Credits
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

How to build KangOS for your device - Tutorial
==============================================

Downloading KangOS Source Codes
-------------------------------

To get started with the building process, you'll need to get familiar with [Git and Repo](http://source.android.com/source/using-repo.html).

To initialize your local repository, use a command like this:

```bash
repo init -u https://github.com/Kang-OS-R/android_manifest -b eleven
```
To save time, space and internet data during sync, use a command like this:

```bash
repo init --depth=1 -u https://github.com/Kang-OS-R/android_manifest -b eleven
```

Then to sync up
---------------

```bash
repo sync -c --force-sync --no-tags --no-clone-bundle -j$(nproc --all) --optimized-fetch --prune
```

KangOS Flags
------------

- USE_GAPPS := true, use this flag to make GApps Build.

- Screen-Off FOD, FOD Animation and Icon Picker support is there in ROM Source, just add appropriate strings in your device tree to enable them.

- TARGET_OPLAUNCHER := true, use this flag for including OnePlus Launcher ported by @MrSluffy in your KangOS build.

Finally to build
----------------

From root directory of Project, perform following commands in terminal


```bash
. build/envsetup.sh
lunch kangos_<devicecodename>-userdebug
make bacon
```
-----------------------------------------------------------------------------

A Detailed Overlook About Setting Up Your Machine For Compilation:
==================================================================

>> To get started with the building process, you'll need to get familiar with [Git and Repo](http://source.android.com/source/using-repo.html).

Build Environment
-----------------

- Tested and Working on any version of Ubuntu - 14.04, 14.10, 15.04, 16.04, 18.04, 20.04 (64-bit)
- Any other distribution based of the Ubuntu Distro such as Lubuntu, Xubuntu and etc.
- Any form of Terminal
- Decent hardware (minimum of at least a quad core CPU and 16 GB of RAM)
- A storage unit of any kind (We recommend utilizing SSDs as Mechanical HDDs slow down the build proccess drastically and the minimum storage size is 70GB. Having more will be useful with CCache[More on that later])
- Required Packages should have been installed

### Required Packages [this is for ubuntu 16.04, for other variants it may differ]
##### Simply copy and paste this in a terminal window:
>> [Hint: This command updates the Ubuntu Packages List (Install Listing) and install the required version of Java]

```bash
     sudo apt-get install openjdk-8-jdk
```
>> [Hint: Running this command installs the other required packages to build android]

```bash
     sudo apt-get update && sudo apt-get install bc git-core gnupg flex bison gperf libsdl1.2-dev libesd0-dev libwxgtk3.0-dev squashfs-tools build-essential zip curl libncurses5-dev zlib1g-dev openjdk-8-jre openjdk-8-jdk pngcrush schedtool libxml2 libxml2-utils xsltproc lzop libc6-dev schedtool g++-multilib lib32z1-dev lib32ncurses5-dev lib32readline6-dev gcc-multilib maven tmux screen w3m ncftp adb fastboot repo python default-jdk
```

Grabbing the sources
====================

- Making required directories
- Obtaining the repo binary
- Adding repo binary to your path
- Giving the repo binary proper permissions
- Initializing an empty repo
- Syncing the repo

>> Alright, so now we’re getting there. I have outlined the basics of what we’re about to do and broke them down as I know them. This is all pretty much going to be copy/paste so it’ll be fairly difficult to screw this up :)

Make directory for the repo binary
----------------------------------

```bash
      mkdir ~/bin
```

Add directory for the repo binary to its path
---------------------------------------------

```bash
      PATH=~/bin:$PATH
```

Downloading repo binary and placing it in the proper directory
--------------------------------------------------------------

```bash
      curl http://commondatastorage.googleapis.com/git-repo-downloads/repo > ~/bin/repo
```

Giving the repo binary the proper permissions
---------------------------------------------

```bash
      chmod a+x ~/bin/repo
```

Creating directory for KangOS source codes to be synced and compiled
--------------------------------------------------------------------

```bash
      mkdir ~/kangos
      cd ~/kangos
```

Another Simple Script For Setting Up Build Environment
======================================================

```bash
      sudo apt update && sudo apt upgrade
      git clone https://github.com/akhilnarang/scripts --depth 1
      cd scripts
      bash setup/android_build_env.sh
```

-----------------------------------------------------------------------------------------------

After Succesfully Compiling KangOS for your device, dont forgot to take a look at this : 

>> To get official maintainership for KangOS, refer [**here**](https://telegra.ph/Apply-for-KANG-OS-Official-04-27).

>> Contact us via   <a href="https://t.me/kangos">
<img src="https://img.shields.io/badge/Telegram-Chat-blue?style=for-the-badge">


