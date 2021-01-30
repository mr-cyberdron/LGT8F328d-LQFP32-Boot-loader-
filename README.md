# LGT8F328d-LQFP32-Boot-loader-
This repository contains files and instructions, that can help you with installation bootloader on arduino nano compartable board "LGT8F328d-LQFP32"

To burn bootloader you need 
1) Download arduino IDE https://www.arduino.cc/en/software
2) Install packets of lgt8fx boards during this link https://github.com/dbuezas/lgt8fx#start-of-content
3) Unzip LarduinoISP-master.zip and run sketch LarduinoISP
4) Burn arduino uno/nano with this cketch
5) At the next step you need  to download Octobot IDE http://wiki.ocrobot.com/doku.php?id=en:downloads
6) Unzip Octobot IDE andd replacing.zip, 
7) Copy floders to \ocrobot-0005-windows\hardware\avr\bootloaders
8) Copy boards.txt  to \ocrobot-0005-windows\hardware\avr (MAKE the BACKUP!)
9) Replasing used because octobot dont have bootloaderfiles for aimed controller, to change board, you can change boards.txt, begining from this line "alpha8f328d.name=Ocrobot Alpha 8F328p"
10) Open octobot, set settings: board:Ocrobot Alpha 8F328p, serial port: (arduino uno/nano) , programmer: Arduino as ISP
11) Connect arduino to burned board due to next scheme :
![](https://image.geek-workshop.com/forum/201604/03/110353eiiwydix7fx7aw7t.png)
12) Choose blink scetch and try upload if all is ok go to 13 point if not, try to upload with boards.txt backup, or change parameters in this file for you board 
for example:
this:
328.menu.variant.modelD_SSOP20=328D-SSOP20 (e.g. green pro mini alternative)
328.menu.variant.modelD_SSOP20.bootloader.path=lgt8fx8e
328.menu.variant.modelD_SSOP20.bootloader.file=lgt8fx8e/optiboot_lgt8f328d.hex
into this:
328.menu.variant.modelD_SSOP20=328P-SSOP20 (e.g. green pro mini alternative)
328.menu.variant.modelD_SSOP20.bootloader.path=lgt8fx8ps20
328.menu.variant.modelD_SSOP20.bootloader.file=lgt8fx8ps20/optiboot_lgt8f328ps20.hex

13) Reconect USB cable and click tools>burn bootloader, if something wrong go to item 10
14) If burning OK try flash scketch from arduino IDE
15) Have Fun
16) Support autor: http://qiwi.com/p/380937122470


