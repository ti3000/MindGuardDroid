# MindGuardDroid
Mind Guard Droid 2023 is a revival of the popular method of installing MindGuard on Android
# Mind Guard Droid 2023

## Introduction

Mind Guard Droid 2023 is a revival of the popular method of installing MindGuard on Android. It is an Android terminal emulator and Linux environment app that works directly with no rooting required. MindGuard is a software program that provides mind control protection, and it is based on the original code by Lyle Zapato. Mind Guard Droid 2023 contains MindGuard v0.0.05 by Github user Asbestomolesto.

## System Requirements

Android minimum system requirements:
- Android v7 and above (lower versions not supported)
- ARM architecture
- 2GB RAM
- 4GB free storage space
- Internet connection

## Installation

Follow these steps to install Mind Guard Droid 2023:

1. Install Termux app on Android >= 7 from [GitHub](https://github.com/termux/termux-app) or [F-Droid](https://f-droid.org/en/packages/com.termux/)
2. Check your device architecture by running the following command in Termux: `uname -m`
3. Download the Termux backup file from the [GitHub release page](https://github.com/mindguard-droid-2023/mindguard-android-2023/releases) (file name: termux-backup-tar.gz, file size: 853MB)
4. Move the downloaded file to the root of the internal storage
5. Open Termux and run the following commands:

```
pkg update
pkg install root-repo
pkg install x11-repo
termux-setup-storage
tar -zxf /sdcard/termux-backup.tar.gz -C /data/data/com.termux/files --recursive-unlink --preserve-permissions
```

6. Set up VNC with the following settings: Address: 127.0.0.1:5901, Password: 12345678
7. Start the Mind Guard Droid distro by running `./start-debian.sh` in Termux

## Known Issues

- VNC server start error (warning: localhost:1 is taken because of /tmp/.X1-lock or /tmp/.X11-unix/X1)

Solution:
```
rm /tmp/.X1-lock
rm /tmp/.x11-unix/X1
```

If the above solution does not work, you can try using a different display number (e.g. `vncserver :2`).

## Credits

We would like to give credit to the following:

- Lyle Zapato (MindGuard Developer)
- Asbestomolesto (GTK error fix)
- Termux
- VNC
- TI Community

## Links

- [Sourceforge Backup](https://sourceforge.net/projects/mindguarddroid/)
- [MindGuard YouTube Channel](https://www.youtube.com/@mindguarddroid)
- [WebSite](https://sites.google.com/site/mindguarddroid/)
- [Developer TI3000 Facebook](https://www.facebook.com/teye.threethousand/)