
# DevResources

**Default debug keystore location**

/Users/{user_name}/.local/share/Xamarin/Mono\ for\ Android/debug.keystore

**Generate sha256**

keytool -list -v -keystore /Users/{user_name}/.local/share/Xamarin/Mono\ for\ Android/debug.keystore -alias androiddebugkey -storepass android -keypass android

**VSTS mobile tasks**

**Redths Obliterate tool**

Official repo - <https://github.com/Redth/XamarinStudio.RedthsAddin>

VSTS mobile tasks repo - <https://github.com/jamesmontemagno/vsts-mobile-tasks>

1. [ADB Tips](AdbTips.md)

2. [iOS terminal Tips](iOSTips.md)

**Downgrading Xamarin**

Find the branch name from <https://docs.microsoft.com/en-gb/xamarin/ios/release-notes/>
1. Xamarin.iOS artifacts - <https://jenkins.mono-project.com/view/Xamarin.MaciOS/>
2. Xamarin.Android artifacts - <https://jenkins.mono-project.com/view/Xamarin.Android/>
