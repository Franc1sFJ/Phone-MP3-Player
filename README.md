# Phone-MP3-Player
Trying to turn an old android phone into an MP3 player. Work in progress. End result might not be ideal.

### Device
Device model: Motorola One Macro

Android version: 10

### KnownDevice Issues:
No power button

Charging port issues

Call screen hang issues

Things you require:
+ Developer mode enabled
    + USB debugging turned on
+ sdk platform tools on your PC

## How to go about the process

### Step 1: Factory Reset

Settings --> System --> Advanced --> Reset options --> Erase all data (factory rest)

This resets your phone and removes all existing data. So, **make sure to backup all necessary files** before this process.

### Step 2: Initial Setup
Setup your phone as you normally would, keeping in mind that this will be your MP3 player. Applications will be included by default and you will have to sign into your Google account to access the playstore and download required applications if that is your preferred method.

### Step 3: Downloads and Updates
Ensure that you update your system and download the required music playing and streaming apps onto your device.

### Step 4: Uninstalling and Disabling apps
Now, you can go ahead and uninstall all the unnecessary apps. Some apps cannot be uninstalled. In this case, press and hold the app. Then, press info. Then go ahead and disable the app. This removes it from the app list. However, these apps are still on your device.

### Step 5: Enabling Developer options

Settings --> About Phone --> Build Number (Repeatedly tap until developer mode gets enabled)

Settings --> System --> Advanced --> Developer options --> Enable USB debugging

In this process, you can also enable/disable other settings inside and outside of developer option that you think will work better for the intended use of the device.

### Step 6: Getting sdk platform tools
You can get the latest version of sdk platform tools from [Android Developer Studio](https://developer.android.com/tools/releases/platform-tools)
Download sdk tools for your PC and unzip the file in a suitable location.

### Step 7: Running sdk platform tools
Head to the unzipped folder. Once you're insie the folder,
In Windows: Go to the address bar in explorer. Click on it and type `cmd`. Press enter.

In linux: Right click and select Open in Terminal. Run the command `adb devices`. If it says adb not found, use the following command:
```
sudo apt install adb
```

###  Step 8: Using adb
adb is what we will use to remove all the unwanted and disabled apps. First, to make sure that adb works properly and that the mobile device is responsive type in:
```
adb devices
```
This should list the connected device with usb debugging. This will also give a popup on the mobile device asking whether to allow access or not. You can allow access.

To see the exact edvice that you're working with, use:
```
adb devices -l
```

### Step 9: Uninstalling packages
The packages disabled in Step 4 can be completely removed using adb if that is what you prefer. To make sure you're removing the right packages, you need to know the packages. To list the packages on your device, use the command:
```
adb shell pm list packages
```
To only see the disabled packages, you can use the command:
```
adb shell pm list packages -d
```
To uninsatll a package, run the following command:
```
adb shell pm uninstall --user 0 <package name>
```
Replace the `<package name>` with the name of the actual package that you want to uninstall. For example:
```
adb shell pm uninstall --user 0 com.facebook.system
```
