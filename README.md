# acroreadsuse15
Adobe Reader 9.5.5 AppImage for OpenSuSE Leap 15.x

This is a workaround I created for running Adobe Reader 9.5.5 on OpenSuSE Leap 15.x.

Source that helped and inspired me: https://gist.github.com/cho2/79964a49a4f5f545853d3ebdfd1efe73

## Warning
- Currently unable to run on OpenSuSE Leap 15.3
- This is an in-a-rush project so may be sloppy. Any help will be appreciated

## Prerequisite
You need to install glibc-locale-base-32bit before running the appimage:
```
zypper install glibc-locale-base-32bit
```

## How to use
- Fulfill the prerequisite above
- Because of github can't handle file larger than 25MB, so for now I uploaded the file into my drive. Download here --> https://drive.google.com/file/d/1bQbnmi65LBI4CkioxnakPPkAgLdAaUFq
- Right click on the downloaded AppImage file --> Properties --> Permissions --> check "Is executable" --> OK
  or you can simply chmod +x the file
- Run it by clicking it (or by using cli). Be patient, the first time loading it is a bit slow.
- Enjoy!

## How to compile yourself
You can compile appimage on your own (in case having doubt running something suspicious from me). This is my step doing it:
- Download from latest release https://github.com/chrizneko/acroreadsuse15/releases/latest and extract it, copy the content to /home/user/acroreadsuse/
- Download adobe reader source from http://ftp.adobe.com/pub/adobe/reader/unix/9.x/9.5.5/enu/AdbeRdr9.5.5-1_i486linux_enu.tar.bz2 and extract it
- Copy the COMMON.TAR and ILINXR.TAR to /home/user/acroreadsuse/
- Cd to the that directory (/home/user/acroreadsuse)
- Run this: bash -ex pkg2appimageacroread acroread.yml
- Your appimage will be in the folder /home/user/acroreadsuse/out
Note: if you need to change the directory, change the acroread.yml on the line contains "/home/user/acroreadsuse/" into your liking

## Extra notes
- I commented the "delete_blacklisted" line on a regular pkg2appimage bash script, therefore I included it in this repo the pkg2appimage bash script that I changed. So that appimage won't delete the basic library acroread needed when compiling
- Copied libraries that needed by acroread from OpenSuSE Leap 42.3
- Changed the acroread bash script line 50 and line 560 so the program will use the correct library directory and file (see https://gist.github.com/cho2/79964a49a4f5f545853d3ebdfd1efe73#gistcomment-2932886)

## TODO
- Integrate missing libraries and fix wrong libraries loaded, so the prerequisite above can be removed
