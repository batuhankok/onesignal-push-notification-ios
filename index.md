Hey,

I know, Push Notification can be so annoying problem for iOS developers. However, OneSignal makes your life easy to sending notifications by using web interface of OneSignal. The installing process is a little bit hard, so, I have written here to make your life easier!

1. Go to www.onesignal.com
2. Create a app
3. Open new tab, go to developer.apple.com
4. Open _Certificates/Identifiers_
5. Click _App IDs_
6. Add new one
7. Then, edit this app
8. _Open Keychain Access_
9. Request a certificate from a certificate authority 
10. Upload this cert file to editing page (nu.7)
11. Download the certificate and open it
12. Click the certificate that is starting like _IOS Push Services_
13. Right click to this certificate, then export it
14. Return to onesignal.com, upload the .p12 file to OneSignal
15. Open terminal (you can push CMD + Space)
16. Write, `cd` and drag drop the your app folder to terminal, press enter
17. It seems like this: `cd /Users/***/Desktop/XcodeApps/***\ ***` 
18. Write, `ls`, then press enter
19. Write, `pod init`, then press enter
20. Write, `ls`, then press enter
21. Write, `open Podfile`, then press enter
22. Write between do - and, `pod 'OneSignal'` to the file that did opened
23. Write, `pod install`, then press enter
24. Then open your project with clicking example.xcworkspace
25. Open Capabilities, Push capability -> switch on 
26. Background capability -> switch on
27. On the background capability, remote push notification -> switch on
28. Everything is okay.

**Good luck! **