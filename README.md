# Fiddler_Android_SSL1

- Root android
- Install fiddler
- Setup android wifi to use your PC's internatl IP and :8888 as a port
- Open ipv4.fiddler:8888 on android
- Install certificate on android
- Connect phone to pc
- Open cmd and do: adb shell > su > mount -o rw,remount /system
- Navigate to /data/misc/user/0/cacerts-added/ and copy the file name ending with a ".0" extension
- Move the certificate to system storage mv /data/misc/user/0/cacerts-added/xxxxxxxx.0 /system/etc/security/cacerts
- mount -o ro,remount /system
- adb reboot
