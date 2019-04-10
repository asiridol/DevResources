## iOS Command line tips
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
