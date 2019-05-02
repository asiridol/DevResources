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

**Get data folder**
* use this class
 ```
    public static class NSSearchPath
    {
        public static string[] GetDirectories(NSSearchPathDirectory directory, NSSearchPathDomain domainMask, bool expandTilde = true)
        {
            return NSArray.StringArrayFromHandle(NSSearchPathForDirectoriesInDomains((nuint)(ulong)directory, (nuint)(ulong)domainMask, expandTilde));
        }

        [DllImport(Constants.FoundationLibrary)]
        static extern IntPtr NSSearchPathForDirectoriesInDomains(nuint directory, nuint domainMask, bool expandTilde);
    }
    
// usage
var directories = NSSearchPath.GetDirectories(NSSearchPathDirectory.DocumentDirectory, NSSearchPathDomain.All);
System.Diagnostics.Debug.WriteLine("Doc : " + directories.FirstOrDefault());
             ```
