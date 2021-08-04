# acroreadsuse15
Adobe Reader 9.5.5 AppImage for OpenSuSE Leap 15.x

This is a workaround I created for running Adobe Reader 9.5.5 on OpenSuSE Leap 15.x.

Source that helped and inspired me: https://gist.github.com/cho2/79964a49a4f5f545853d3ebdfd1efe73

Warning: currently unable to run on OpenSuSE Leap 15.3

What works:
- Viewing 3D PDF

What doesn't work:
- Looks like printing doesn't work
- etc I don't know, TBH I researched this for the sake of viewing 3D PDF

Prerequisite:
- OpenSuSE Leap 15.0: You need to install glibc-locale-32bit (zypper install glibc-locale-32bit)
- OpenSuSE Leap 15.1 and 15.2: You need to install glibc-locale-base-32bit (zypper install glibc-locale-base-32bit)

How to use:
- Fulfill the prerequisite above
- Because of github can't handle file larger than 25MB, download the bundled appimage from my drive here --> https://drive.google.com/file/d/1bQbnmi65LBI4CkioxnakPPkAgLdAaUFq/view?usp=sharing
- Right click on the downloaded AppImage file --> Properties --> Permissions --> check "Is executable" --> OK
  or you can simply chmod +x the file
- Enjoy!

You can compile appimage on your own. This is my step doing it:
- Download from latest release https://github.com/chrizneko/acroreadsuse15/releases/latest and extract it, copy the content to /home/user/acroreadsuse/
- Download adobe reader source from ftp://ftp.adobe.com/pub/adobe/reader/unix/9.x/9.5.5/enu/AdbeRdr9.5.5-1_i486linux_enu.tar.bz2 and extract it
- Copy the COMMON.TAR and ILINXR.TAR to /home/user/acroreadsuse/
- Cd to the acroread.yml
- Run this: bash -ex pkg2appimageacroread acroread.yml
- Your appimage will be on out folder
Note: if you need to change the directory, change the acroread.yml on the line contains "/home/user/acroreadsuse/" into your liking

TODO:
- Integrate missing libraries and wrong libraries loaded, so the prerequisite above can be removed
