# LGTV-Firmware-Downgrade

This guide will help to walk you through downgrading the Software Version and also webOS to a previous version so you can root/jailbreak webOS on on an LGTV from webOS version 4 to 6.

This has been confirmed to work on an LG 43 Inch TV 2021 Model - LG-43UP75006LF https://www.lg.com/uk/tvs/lg-43up75006lf from Software Version 3.30.10 to 3.21.30 but should work on other LG TV models too with the relevant firmware for that TV.

For the original thread on AV Forums which helped in creating this guide please go here https://www.avsforum.com/threads/guide-lg-webos-tvs-firmware-downgrade-advanced-users-only.3217168/

For more information on the Homebrew Channel please go here https://github.com/webosbrew/webos-homebrew-channel

For more information on how the rooting process works from a technical point of view or if you haven't updated your TV yet then please go here https://github.com/RootMyTV/RootMyTV.github.io/

For the background on why I even did this then please click here for the [Background](https://github.com/reprodev/LGTV-Firmware-Downgrade/edit/main/README.md#background)

# What You'll Need Before Starting

1. An LG TV with Developer Mode App installed and activated https://webostv.developer.lge.com/develop/app-test/using-devmode-app/
2. An LG Developer Account https://webostv.developer.lge.com/develop/app-test/using-devmode-app/
3. Homebrew Channel (Optional)
4. A USB thumb drive formatted as FAT32 or NTFS [Setting up your USB Thumb Drive](https://github.com/reprodev/LGTV-Firmware-Downgrade/edit/main/README.md#setting-up-your-usb-thumb-drive)
5. Your TV's previous firmware epk file [Getting your Previous Firmware](https://github.com/reprodev/LGTV-Firmware-Downgrade/edit/main/README.md#getting-your-previous-firmware)
6. LG webOS Cli Install Package (Needed for Method 2 and 3) 
7. LG Developer Manager Desktop App https://github.com/webosbrew/dev-manager-desktop (Needed for Method 2 and 3)
8. Downgrade Launch App ipk https://forum.xda-developers.com/attachments/downgrade-launch-app_1-0-0_all-rar.5584169/?hash=f31b04de248f3fd1a0646ed9efa70b50
9. webos4x-6x.expertmode.downgrade IPK http://45.140.167.171/ipk/webos4x-6x.expertmode.downgrade_1.0.0_all.ipk

# Getting your Previous Firmware

**(DISCLAIMER)** Please make sure you get the right firmware for your TV as there will be no checks run when you go to install the file by the TV. This means you could try to install the firmware for a different TV on yours. If you're unsure check the Reference Models on the LG website as one firmware covers several TVs.

1. Go the Korean LG TV Website and using your model number change the end of the address so that you get to your Tv firmware page. If this works you can Skip past this section to the Methods. If this doesn't work then follow the steps below to get the correct firmware for your TV.
2. In this example we are downgrading to 3.21.30 so go to this link https://www.lg.com/uk/support/product/lg-43UP75006LF.AEKD for the TV from the UK LG site or wherever you are based
3. On this page scroll down to the bottom right and click on the reference link under the Software download which will open in a new window and linked here https://www.lg.com/uk/support/product/lg-43UP75006LF.AEKD#software_drivers_reference_2
4. All of the models listed can use that firmware and so can your TV so keep a note of these somewhere as you may need them for Step 5.
5. Go to the Korean LG TV Website Driver Support section and then translate to English. Linked here https://www.lge.co.kr/support/product-manuals?title=driver&mktModel
6. You can then search for the TV by using the Dropdown menu on the left to select Tv/Projectors and then the type of TV you have on the right. In this example, it would be Ultra HD and then you type "43" in the search to find a model on the page in the list. One of these will match the ones listed in the reference for your firmware.
7. Once you are on the firmware page you will have all the previous versions for your TV, if you are sure that this is the correct one for your TV based on the reference then download the zip file.
8. **(DISCLAIMER)** Make sure this is the correct file for your TV before and correct version that you want. I would suggest you also download the latest firmware for your TV in case you need to get back to the latest firmware at a later date. Once you have these zip files downloaded make sure you have a backup of them somewhere like a Dropbox/USB Hard-drive as there is always the chance that these files will be removed at some point from the official site.

You should now have the correct previous firmware for your LG TV downloaded and have it backed up so we can move onto setting up your USB thumb drive.

# Setting up your USB Thumb Drive

1. Connect your thumb drive up to the PC you downloaded the firmware onto
2. Format the thumb-drive to either FAT32 or NTFS as no other formats will work. Please note this will wipe all data which is already on the drive so make sure you back this up somewhere first if it's important.
3. Once formatted, create a folder on root of the USB thumb drive called "LG_DTV"
4. Open up the zip file with the firmware you downloaded, in this example it would be the 3.21.30 firmware we want to downgrade to. When opened the zip file should contain a file with the extension epk inside.
5. Copy this epk file into the "LG_DTV" folder on the root of the USB thumb drive and wait for it to copy over.
6. Once copied, safely remove the drive from your PC and plug it into your TV. The TV will prompt you to read the files on the drive but you can just exit this to get back to the Home Menu.

You should now have a USB thumb drive set up to use on your LG TV with the correct previous firmware that you want to roll back to in the correct folder. We can now move onto the 3 methods that will let you initiate the downgrade or you can set up Developer Mode now.

# Setting up Developer Mode

This falls slightly outside the scope of this guide but this link will take you to the Offical LG webOS Development site if you haven't gone there already. It will go through of getting Developer Mode installed on the TV and also your PC. You will need Developer Mode installed and Command Line Access to your TV for Method 2 or 3.
Please note it is not required for Method 1 so you can skip this section if that one works for you.

# Let's Downgrade

**DISCLAIMER** Please be aware that all these methods are risky and this could go wrong. Downgrading the software and firmware on your LG TV is not supported officially by LG. Your mileage may vary and although this has worked for my LGTV model twice and should work for you. This may void your warranty and cause you to need a new TV.

# Method 1 - webOS App Club Online Downgrade through the LG TV Web Browser

1. Go to https://webosapp.club/downgrade/ on your TV in the Web Browser. It should open up a dialog on screen asking if you want to connect to webos and share information with them. 
2. Please click Yes/OK here and the website will try to get you to the Software Update screen.
3. If this methods works, you will be able to select the firmware file from your USB Thumb drive on the TV screen to let you install the firmware you downloaded earlier. It will take up to 10 minutes and you will get a notification telling you when it's installed and asking you to click ok to reboot.
4. If this just goes to a black screen or just reboots back to the Home Menu or Live TV then try Method 2

# Method 2 - Install a Downgrade IPK File using Developer Mode

1. Go to http://45.140.167.171/ipk/ on your PC and you will have a list of useful ipk files that can be installed.
2. Translate the website to English and search the page for "webos4x-6x.expertmode.downgrade_1.0.0_all.ipk"
3. Download the webos4x-6x.expertmode.downgrade_1.0.0_all.ipk file to your PC
4. Go to https://forum.xda-developers.com/attachments/downgrade-launch-app_1-0-0_all-rar.5584169/?hash=f31b04de248f3fd1a0646ed9efa70b50 to download a rar file containing "downgrade.launch.app_1.0.0_all.ipk"
4. Set up Developer Mode by following these instructions on your TV if you haven't already. During setup you will get instructions on how to connect your PC to your TV.
5. Install the "webos4x-6x.expertmode.downgrade_1.0.0_all.ipk" ipk file using Dev Manager and it will show up at the end of the list of your Apps.
6. Open the App and if this methods works for you then it will ask you to confirm if you want to access Expert Mode. If successful, you will be able to select the firmware file from your USB Thumb drive on the TV screen to let you install the firmware you downloaded earlier. It will take up to 10 minutes and you will get a notification telling you when it's installed and asking you to click ok to reboot.
7. If this just goes to a black screen or just reboots back to the Home Menu or Live TV then restart the TV and uninstall "webos4x-6x.expertmode.downgrade_1.0.0_all.ipk".
8. Install "downgrade.launch.app_1.0.0_all.ipk" using Dev Manager like before and it will show up at the end of the list of your Apps.
9. Open the App and if this methods works for you then it will ask you to confirm if you want to open Software Update. If successful, you will be able to select the firmware file from your USB Thumb drive on the TV screen to let you install the firmware you downloaded earlier. It will take up to 10 minutes and you will get a notification telling you when it's installed and asking you to click ok to reboot.
10. If this just goes to a black screen or just reboots back to the Home Menu or Live TV then try Method 2

# Method 3 - Send a command via the webOS TV Cli

1. Set up Developer mode if you haven't already done so and then open up the Developer Mode App on your TV
2. Connect to your TV using the webOS Cli using this command the below command entering your IP address shown on screen. The password to connect with is the passphrase shown on screen in the Developer Mode app

<code> - ssh -p 9922 -i ~/.ssh/tv_webos prisoner@(YOURLGTVIPADDRESS) bash -i </code>
 
3. Send the luna command for opening up the Software Updater program

<code> luna-send-pub -d -n 1 -f "luna://com.webos.applicationManager/launch" '{ "id": "com.webos.app.softwareupdate", "params": { "mode": "user", "flagUpdate": true } }' </code>

4. If this methods works for you then it will ask you to confirm if you want to access Expert Mode. If successful, you will be able to select the firmware file from your USB Thumb drive on the TV screen to let you install the firmware you downloaded earlier. It will take up to 10 minutes and you will get a notification telling you when it's installed and asking you to click ok to reboot.

5. If this just goes to a black screen or just reboots back to the Home Menu or Live TV then you may be out of luck.

# Final steps before root

1. Once you have managed to roll back to a rootable firmware then you will need to uninstall the Developer Mode app from your LG TV. You can do this usually by holding on the icon in the list and then pressing up to get to the "Bin" icon. You will be asked if you are sure you want to delete Developer Mode.
2. Go to Settings -> System -> System Update -> Check that you are on the correct firmware and also make sure that "Auto Update" is switched off here before you root so you don't accidentally update again.

# It's rooting time

1. Go to https://rootmy.tv/ on your LG TV and "Slide to Root" if you have a magic remote or click on the button in the middle/ press 5 if you are using a regular LG TV remote.
2. Once rooted, the TV will reboot once, when it does the first time make sure you open the "Home Screen". This is where the notifications and prompts will be shown for the root and Homebrew Channel install. 
3. After the second reboot you will get the Homebrew Channel added to the end of the list of your Smart Apps towards the right.
4. Open up the Homebrew Channel and click the cog at the top right of the screen to get to the Settings. You should now see listed on the left "Root Status" as ok and your webOS version.
5. This should also automatically switch on SSH with the root user and the default password at "alpine" until you import your SSH keys. More information about this is at https://github.com/RootMyTV/RootMyTV.github.io in their Post Installation Advice

# FAQ

### Do I need to Downgrade Firmware to root?

If you have upgraded to Software Version 3.30 from May 2022 then the original exploit has been patched out. You can still use Developer Mode to get some of the functions of root but doesn't let you do everything the full root would. This is why we install Developer Mode to get to downgrade but then it's removed after root.

### What else do I need to know about the root install e.g. how do I get rid of it all?

The FAQ section on RootMyTV covers most of these questions and is outside the scope of this guide for Software Firmware Downgrade. Please click here for more information https://github.com/RootMyTV/RootMyTV.github.io but a full factory reset of your TV should remove it all for you.

### Can I brick my TV?

The downgrade and root are both risky and could result in your TV bricking but there is a failsafe in the root program that does protect you slightly. More information about "Failsafe Mode" can be found at https://github.com/RootMyTV/RootMyTV.github.io

### What if this doesn't let me downgrade at all?

It took me a few tries to get to the Software Update screen but once I got there it let me do it twice. If this doesn't work for you then it may just be that your TV has had these methods fully patched.

### How do I donate to you?

For now I will be working this out to make it as easy as possible if you want to throw a few bucks my way but it may end up being GitHub Sponsors once I get it working.

# Background

I bought the LG 43 Inch TV 2021 Model - LG-43UP75006LF from Argos in the UK for £250 on sale in June 2022 after accidentally breaking an older LG model while moving. When I first got this TV I was unaware of the Root access and modifications over at rootmy.tv and so just updated as normal.

I had already updated the firmware twice from 3.20 to 3.30.14 As of June 2022 this is the latest firmware which has the exploit patched out. 

When I tried to roll back I found a lot of information spread across the net and mainly in Russian.

The 3.30.14 firmware means that you can only use the developer mode to make any changes and this has to be updated every 50 hours. This would also occasionally delete installed ipk files. For some reason the IFTT web access token wasn't working for me and the auto Developer mode took away my OTT Play IP TV Setup which will be linked here once complete

I had SSH access through Developer Mode and was able to do a few things here and there like install some applications and some remote shortcuts but no root access. This was quite frustrating as I wouldn't have updated if not and it seems like the downgrade option is now patched out as well as the exploit from Rootmy.tv

I searched through the Russian forums for information but most of the really informative information is in Russian and linked below.

Following Method 2 after trying Method 3 a few times I was able to get the Software Update screen to open but then installed a version of the firmware that was one version back to many. Once installed I was unable to open the Web Browser and was being asked to update my Firmware.

I found the later 3.20.14 and used this instead with Method 2 and replaced this on the USB thumbdrive to do the upgrade. This version let me open the Web Browser and go to https://rootmy.tv to perform the root install as normal. I tested it after by installing some IPKs and other fun stuff

## Special Thanks and References:

### AVS Forum LG TV Firmware Downgrade Thread

https://www.avsforum.com/threads/guide-lg-webos-tvs-firmware-downgrade-advanced-users-only.3217168/

### LG TV Firmware Rollback Thread from Russian WebOS Forums:

http://webos-forums.ru/topic3157.html

## Developers from Russian webOS Forums

### Jack Sparrow : 

http://webos-forums.ru/jacksparrow-u8940.html

### Mixmar : 

http://webos-forums.ru/mixmar-u2483.html

### How To Downgrade Software for OLED65CX61A from XDA Developers Site

https://forum.xda-developers.com/t/how-downgrade-software-oled65cx6la.4376371/

# Finally!

Please go ahead and follow me for more and feel free to comment on if this works for you, if you've found a way to make this process better or if there is anything in here that needs to be amended to make it flow better. I'd love to hear from anyone that has given this a try

Yours technially,
ReproDev
