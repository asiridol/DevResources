
# DevResources

**Default debug keystore location**

/Users/{user_name}/.local/share/Xamarin/Mono\ for\ Android/debug.keystore

**Generate sha256**

keytool -list -v -keystore /Users/{user_name}/.local/share/Xamarin/Mono\ for\ Android/debug.keystore -alias androiddebugkey -storepass android -keypass android

**VSTS mobile tasks**

VSTS mobile tasks repo - <https://github.com/jamesmontemagno/vsts-mobile-tasks>


### ADB tips

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

### iOS Command line tips
**Get app container from simulator**

xcrun simctl get_app_container booted _bundle_id_

**List all simulators**

xcrun simctl list --json

**Screen record**

xcrun simctl io booted recordVideo — type=mp4 ./test.mp4

**Screenshot**

xcrun simctl io booted screenshot ./screen.png

**Simulate url open**

* xcrun simctl openurl booted _https://google.com_ - absolute urls
* xcrun simctl openurl booted _myapp://_ - deep links
