# acroreadsuse15
Adobe Reader 9.5.5 AppImage for OpenSuSE Leap 15.x

This is a workaround I created for running Adobe Reader 9.5.5 on OpenSuSE Leap 15.x.

Source that helped me: https://gist.github.com/cho2/79964a49a4f5f545853d3ebdfd1efe73

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
- Download release here --> 
- Right click on the downloaded AppImage file --> Properties --> Permissions --> check "Is executable" --> OK
  or you can simply chmod +x the file
- Enjoy!

TODO:
- Integrate missing libraries and wrong libraries loaded, so the prerequisite above can be removed
