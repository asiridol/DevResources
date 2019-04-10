
# DevResources

**Default debug keystore location**

/Users/{user_name}/.local/share/Xamarin/Mono\ for\ Android/debug.keystore

**Generate sha256**

keytool -list -v -keystore /Users/{user_name}/.local/share/Xamarin/Mono\ for\ Android/debug.keystore -alias androiddebugkey -storepass android -keypass android

**VSTS mobile tasks**

VSTS mobile tasks repo - <https://github.com/jamesmontemagno/vsts-mobile-tasks>

(ADB Tips)[AdbTips.md]

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
