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

1. Install Termux app on Android from [F-Droid](https://f-droid.org/en/packages/com.termux/) or [GitHub](https://github.com/termux/termux-app)
2. Check your device architecture by running the following command in Termux: `uname -m`
3. Download the Termux backup file from the [GitHub release page](https://github.com/ti3000/MindGuardDroid/releases/tag/mindguard) (file name: termux-backup-tar.gz)
4. Move the downloaded file to the root of the internal storage
5. Open Termux and run the following commands:

```
pkg update
pkg install root-repo
pkg install x11-repo
termux-setup-storage
tar -zxf /sdcard/termux-backup.tar.gz -C /data/data/com.termux/files --recursive-unlink --preserve-permissions
```
6. Start the Mind Guard Droid distro by running `./start-debian.sh` in Termux

7. Start VNC Server with `vncserver-start` command

Set up VNC App with the following settings: 
```
Address: 127.0.0.1:5901
Password: 123456
```
## Known Issues

- VNC server start error (warning: localhost:1 is taken because of /tmp/.X1-lock or /tmp/.X11-unix/X1)

Solution:
``` 
vncserver-stop
rm /tmp/.X1-lock
rm /tmp/.x11-unix/X1
vncserver-start
```

If the above solution does not work, you can try using a different display number (e.g. `vncserver :2`).
```
export DISPLAY=":1"
```

## Credits

We would like to give credit to the following:

- Lyle Zapato (MindGuard Developer)
- TI Community

## Links

- [Sourceforge Backup](https://sourceforge.net/projects/mindguarddroid/)
- [Google Drive Backup](https://drive.google.com/uc?export=download&id=1foFRbiPhuYTcepLf0kilyMN3zVMYlPj0)
- [MindGuard YouTube Channel](https://www.youtube.com/@mindguarddroid)
- [MindGuard OS WebSite](https://sites.google.com/site/mindguarddroid/)
- [Developer TI3000 Meta](https://www.facebook.com/teye.threethousand/)
