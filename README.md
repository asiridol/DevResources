
# Dev Resources

**Default debug keystore location**

/Users/{user_name}/.local/share/Xamarin/Mono\ for\ Android/debug.keystore

**Generate sha256**

keytool -list -v -keystore /Users/{user_name}/.local/share/Xamarin/Mono\ for\ Android/debug.keystore -alias androiddebugkey -storepass android -keypass android

**VSTS mobile tasks**

VSTS mobile tasks repo - <https://github.com/jamesmontemagno/vsts-mobile-tasks>

**Redths Obliterate tool**

Official repo - <https://github.com/Redth/XamarinStudio.RedthsAddin>

**Terminal Tips**

1. [ADB Tips](AdbTips.md)

2. [iOS terminal Tips](iOSTips.md)

**Better Vysor for Android**

[Genymobile Screen Mirror](https://github.com/Genymobile/scrcpy)

**Downgrading Xamarin**

Find the branch name from <https://docs.microsoft.com/en-gb/xamarin/ios/release-notes/>
1. Xamarin.iOS artifacts - <https://jenkins.mono-project.com/view/Xamarin.MaciOS/>
2. Xamarin.Android artifacts - <https://jenkins.mono-project.com/view/Xamarin.Android/>
3. Or use https://github.com/jonathanpeppers/boots

**Resolving provisioning profile issues**

<https://gist.github.com/asiridol/ae2ff43b83cb6216878bef056ffad17e>

**Misc Resources**
1. [Android Resources](AndroidTuts.md)
1. [iOS Resources](iOsTuts.md)
1. [Xamarin Specific tips](CrossPlatform.md)
1. [Other Misc. Resources](OtherTuts.md)
1. [Pen testing tools and resources](PenTest.md)
