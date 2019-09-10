## ADB tips

**Screen record**

* adb shell screenrecord /sdcard/video.mp4
* then pull the mp4 file

**Screnshot**

* adb shell screencap -p > myfile.jpg
* then pull the jpg file

**Get all activities in the stack**

adb shell dumpsys activity activities | grep _package_name_ | grep Hist

**Get current top most activity**

adb shell dumpsys window windows | grep -E 'mCurrentFocus|mFocusedApp'

**Access package folder of a debug app**

adb -s _device_id_ shell run-as _package_name_

**Copy database file in package folder of a debug app**
adb -d shell "run-as com.example.test cat /data/data/com.example.test/databases/data.db" > data.db

_Note - Sometimes it's necessary to download the temp files created by sqllite (*.db-shm, *.db-wal)_

**ADB over wifi**
Connect device via USB

* ./adb tcpip 5555
* ./adb shell ifconfig - get ip address
* ./adb connect xxxxxxxx:5555

**List all packages on a device**

adb -s _device_id_ shell pm list packages

**Get main activity**

adb  shell dumpsys package _package_name_ |grep "android.intent.action.MAIN:" -A1 | tail -n 1

**Check package flags**
adb -s _device_id_ shell dumpsys package _package_name_ |grep pkgFlags

**Install apk**

* adb install _path_to_apk_
* adb -s _device_id_ install _path_to_apk_

**Uninstall apk**
* adb uninstall _package_name_ - will clear data
* adb uninstall -k _package_name_

**Pull apk from device**
* adb shell pm list packages - get all packages
* adb shell pm path _package_name_ - get apk path
* adb pull _apk_path_ _destination_path_
* adb install-multiple /directory_name/*.apk _(Sometimes the apk (debug) is splitted in to small chunks of apk files. In that case pull all of the apk files in to a folder and then run this instead)_

**Check certificate used to sign an apk**
* pull apk from device (if needed)
* unzip apk file using _unzip {filename}.apk_
* navigate to META-INF directory
* run _keytool -printcert -file APKSIGNE.RSA_

**Simulate deeplinks**

adb shell am start -a android.intent.action.VIEW -d _deep_link_
