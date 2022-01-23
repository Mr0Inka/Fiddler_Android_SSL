# Fiddler_Android_SSL1

- Root android
- Install fiddler
- Setup android wifi to use your PC's internatl IP and :8888 as a port
- Fiddler > Tools > Export Root Certificate 
- CMD to desktop
- openssl x509 -inform der -in FiddlerRoot.cer -outform PEM -out FiddlerRoot.pem
- openssl x509 -hash -noout -in  FiddlerRoot.pem
- Rename file to <hash>.0
- Connect phone to pc
- Open cmd and do: adb shell > su > mount -o rw,remount /system
- Move .0 file to the phone's internal storage
- Move the certificate to system storage mv /sdcard/035f9290.0 /system/etc/security/cacerts
- mount -o ro,remount /system
- adb reboot
