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
