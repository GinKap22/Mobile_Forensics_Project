TCM Security : Mobile Application Penetration Testing (MAPT) / 24th November 2026

OS: Windows 11

Android Emulator : Nexus 5 , Android 10.0 ("Q") x86_6 , API 29

Android Studio : Download InjuredAndroid 
  * App is not available from play store at the moment
  * Found the github repository but its in archived already and read-only mode 
      https://github.com/B3nac/InjuredAndroid/releases/tag/v1.0.12
<img width="1211" height="625" alt="Screenshot 2026-11-24 150533" src="https://github.com/user-attachments/assets/32afa45f-f2e2-4378-b0c3-f810325eb160" />

 * Downloaded APK and drag and drop to emulator then installed.
<img width="272" height="503" alt="image" src="https://github.com/user-attachments/assets/10ae748b-049b-486c-908f-973eedf315ef" />

Started using ADB in the emulator
Command : adb shell , whoami , ls


<img width="1217" height="590" alt="image" src="https://github.com/user-attachments/assets/8825b87a-a3ca-4e26-ba4d-d510470c64fb" />

cmd : pm list packages


<img width="503" height="264" alt="image" src="https://github.com/user-attachments/assets/d107a3fc-a805-4626-9a96-abd9ffae96f9" />

cmd : pm list packages | grep injured  // or just use CTRL+F :)


<img width="347" height="44" alt="image" src="https://github.com/user-attachments/assets/ba7c9262-6838-4f43-8cb8-c52980532b91" />


cmd : pm path b3nac.injuredandroid


<img width="446" height="47" alt="image" src="https://github.com/user-attachments/assets/baae2556-541d-4a20-9671-c324e485a3f1" />

** Created a separate directory folder for pulling the apk then use adb pull to claimed the apk from the emulator

cmd : adb pull /data/app/b3nac.injuredandroid-oOEdJLsKIoiCg0qmJAw6Sw==/base.apk injuredAndroid_pulled.apk
 * named as : injuredAndroid_pulled.apk

<img width="921" height="191" alt="image" src="https://github.com/user-attachments/assets/c516e8ba-963c-49cb-8b4a-a414e31b7a0c" />

Opened JADX for checking, load the .apk file. 

<img width="886" height="502" alt="image" src="https://github.com/user-attachments/assets/38cc894a-95b3-4509-9718-43eb885cd141" />


It will show everything related to the apk file. From source code,resources, apk signatures, etc..
entire apk to our local machine ready for analysis.


<img width="862" height="680" alt="image" src="https://github.com/user-attachments/assets/0587a201-2a0a-4513-8e16-7db9214c4f3d" />


Just follow the same technique to pull apk from play store using ADB commands.


Often hardcoded strings can be found in resources/strings.xml, xml.xml,source code. Using 
text search feature to search or filter and identify some sensitive information

FlagOne

<img width="271" height="500" alt="image" src="https://github.com/user-attachments/assets/72cc82fe-883b-4b69-9cb9-5047dbc9466b" /> <img width="275" height="505" alt="image" src="https://github.com/user-attachments/assets/75aecec3-e8bc-4dbb-9a5d-de4a0d3911df" />

<img width="1277" height="683" alt="image" src="https://github.com/user-attachments/assets/7d5c2c53-2a45-4fca-8ff8-dc4799f3b755" />


Flagtwo

<img width="269" height="505" alt="image" src="https://github.com/user-attachments/assets/b23353f5-f319-4398-8040-b2b91780beb5" /> <img width="272" height="502" alt="image" src="https://github.com/user-attachments/assets/5ba1e76d-782a-4ab3-835e-fa9d2a5a7666" />




<img width="1278" height="683" alt="image" src="https://github.com/user-attachments/assets/56db563b-076c-4275-875a-42342a4dbb84" />


<img width="847" height="188" alt="image" src="https://github.com/user-attachments/assets/a618be1e-ebf2-480f-be53-75f9a9992a75" />


<img width="311" height="503" alt="image" src="https://github.com/user-attachments/assets/ba649331-9a1f-4b94-a8eb-676f9507b34b" />


















Found some altrnatives (not yet tried)
1. AndroGoat / https://github.com/satishpatnayak/AndroGoat
2. DIVA / https://github.com/payatu/diva-android
3. OVAA / https://github.com/oversecured/ovaa
4. InsecureBankv2 / https://github.com/dineshshetty/Android-InsecureBankv2
5. OWASP MASTG Hacking Playground / https://github.com/OWASP/MASTG-Hacking-Playground


