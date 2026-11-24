# Mobile_Forensics_Project
"Centralized. Organized. Preserved" - First Project for Mobile Forensics Journey

Android Studio
TCM Course Required : As per the course : Nexus 5
Android studio Rabbit 2 doesn't have any more of those Nexus 5

  Download a Google Play System Image **(fIRST sTEP)**

    1. In Android Studio, open Tools > SDK Manager.
    2. Go to the SDK Platforms tab and check Show Package Details in the bottom-right corner.
    3. Expand your desired Android version (e.g., Android 10.0 (Q)) and check a system image labeled Google Play (such as Google Play            Intel x86 Atom System Image or Google Play ARM 64 v8a System Image, depending on your computer's CPU).
    4. Click Apply / OK to download and install it
    
  Best option is to create a custom device
    1. Open Device Manager and click + (Create Virtual Device).
    2. Click New Hardware Profile (or Create Hardware Profile) at the bottom left of the window.
    3. Manually enter the old phone's specs—for a Nexus 5, set Screen Size to 4.95 inches, Resolution to 1080 x 1920 px,and RAM to            2048MB.
    4. Click Finish to save your custom profile and pair it with your desired system image.  

    Enable Play Store in config.ini
    
    1. In Device Manager, click the three dots (⋮) next to your new custom device and select Show on Disk.
    2. Open the config.ini file with any plain text editor (like Notepad or TextEdit).
    3. Find and change (or add) these four lines to match the system image you downloaded in Step 1:ini
    PlayStore.enabled=true
    image.sysdir.1=system-images\android-29\google_apis_playstore\x86\
    tag.display=Google Play
    tag.id=google_apis_playstore
    Use code with caution.
    (Note: Replace android-29 with your chosen API level—such as android-30 or android-34—and replace x86 with x86_64 or arm64-v8a to match the exact folder path inside your Android Sdk\system-images\ folder. On Mac/Linux, use forward slashes / instead of backslashes \).
    4. Save and close config.ini.

Step 4: Wipe Data and Boot

1. Return to Device Manager in Android Studio (you may need to close and reopen the Device Manager panel for the Play Store icon to appear).
2. Click the three dots (⋮) next to your custom device and select Wipe Data.
3. Click the Play (▶) button to launch the emulator. The Google Play Store app will now be installed in the app drawer.
