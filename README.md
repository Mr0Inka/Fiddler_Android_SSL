# Fiddler_Android_SSL1

1 - Root android
2 - Install fiddler
3 - Setup android wifi to use your PC's internatl IP and :8888 as a port
4 - Open ipv4.fiddler:8888 on android
5 - Install certificate on android
6 - Connect phone to pc
7 - Open cmd and do: adb shell > su > mount -o rw,remount /system
8 - Navigate to /data/misc/user/0/cacerts-added/ and copy the file name ending with a ".0" extension
9 - Move the certificate to system storage mv /data/misc/user/0/cacerts-added/xxxxxxxx.0 /system/etc/security/cacerts
10 - mount -o ro,remount /system
11 - adb reboot
