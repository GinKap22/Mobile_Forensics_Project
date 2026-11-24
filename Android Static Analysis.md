TCM Security : Mobile Application Penetration Testing (MAPT) / 24th November 2026

Pulling an APK fro the google Play Store
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

cmd : pm list packages | grep injured 
<img width="347" height="44" alt="image" src="https://github.com/user-attachments/assets/ba7c9262-6838-4f43-8cb8-c52980532b91" />


Found some altrnatives (not yet tried)
1. AndroGoat / https://github.com/satishpatnayak/AndroGoat
2. DIVA / https://github.com/payatu/diva-android
3. OVAA / https://github.com/oversecured/ovaa
4. InsecureBankv2 / https://github.com/dineshshetty/Android-InsecureBankv2
5. OWASP MASTG Hacking Playground / https://github.com/OWASP/MASTG-Hacking-Playground


