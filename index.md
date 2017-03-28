> Hey,
>
> I know, Push Notification can be so annoying problem for iOS developers. However, OneSignal makes your life easy to sending notifications by using web interface of OneSignal. The installing process is a little bit hard, so, I have written here to make your life easier!


1. Go to [onesignal.com]
    1. Login and click the "Create a new app"
    2. Select "Apple iOS (APNS)"
2. Open new tab, go to [onesignal.com/provisionator]
    1. Click __Get Started__
    2. Login with your Apple Developer Account
    3. Select your app that you want to use push notification, click __Generate__
    4. Click __Download .p12 File__ and __*copy the password*__
3. Turn back to the [onesignal.com]'s tab
    1. Select the file that you have just downloaded
    2. Paste the password to the related input, click __Save__
    3. Select __Native iOS__, then copy __Your App ID__ `(like: 5eb5a37e-b458-11e3-ac11-000c2940e62c)`
4. You can close the web browser
5. Open the __terminal__ (hint: you can push CMD + Space and write terminal...)
    1. Write, `cd ` and drag drop the your app folder to the terminal, press enter
    2. It has to seem like this: `cd /Users/***/Desktop/XcodeApps/***\ ***`
    3. Write, `pod init`, then press enter
    4. Write, `open Podfile`, then press enter
    5. Write between `do` - `and`, `pod 'OneSignal'` to the file that did opened and save it
    6. Write, `pod install`, then press enter
6. Then open your project with clicking __example.xcworkspace__
    1. Open __Capabilities__ tab, Push capability: switch on
    2. Background Capability: switch on
    3. In the Background Capability, remote push notification: switch on
7. Then, edit your __AppDelegate.swift__ like above:

```swift
import OneSignal

func application(application: UIApplication, didFinishLaunchingWithOptions launchOptions: [NSObject: AnyObject]?) -> Bool {

//Add this line. Replace '5eb5a37e-b458-11e3-ac11-000c2940e62c' with your OneSignal App ID (you have just copied.)
OneSignal.initWithLaunchOptions(launchOptions, appId: "5eb5a37e-b458-11e3-ac11-000c2940e62c")

return true
}
```

8. Then, save your Xcode project.

### That's all, brilliant 🎉

#### Good luck 😊💪

[onesignal.com]: https://www.onesignal.com
[onesignal.com/provisionator]: https://www.onesignal.com/provisionator
