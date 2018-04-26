# Force React Native
React Native using the Salesforce Mobile SDK

## Setup
```
$ forcereact create
Enter the target platform(s) separated by commas (ios, android): ios,android
Enter your application name: ForceReactNative
Enter your package name: com.mytrail.react
Enter your organization name (Acme, Inc.): glenndimaliwat.com
Enter output directory for your app (leave empty for the current directory): ForceReactNative
```

### iOS
1. In Xcode, open the `<current_directory>/ForceReactNative/ios/ForceReactNative.xcworkspace` file.
2. In the Project view, navigate to ForceReactNative/ForceReactNative/Classes, then open the AppDelegate.m file.
3. Near the top of the file, replace the default values of `RemoteAccessConsumerKey` and `OAuthRedirectURI` with your own settings.
```objectivec
// Fill these in when creating a new Connected Application on Force.com
static NSString * const RemoteAccessConsumerKey = 
    @"3MVG9Iu66FKeHhINkB1l7xt7kR8czFcCTUhgoA8Ol2Ltf1eYHOU4SqQRSEitYFDUpqRWcoQ2.dBv_a1Dyu5xa";
static NSString * const OAuthRedirectURI = @"testsfdc:///mobilesdk/detect/oauth/done";
```

### Android
1. In the Android Studio Welcome Screen, click `Import Project (Eclipse ADT, Gradle, etc.)`. Or, if another project is already open in Android Studio, choose `File | Open`.
2. Select the <current_directory>/FirstReact/android directory, then click `OK`.
3. In the Project view, open the app/res/values/bootconfig.xml file.
4. Replace the `remoteAccessConsumerKey` and `oauthRedirectURI` values with your own settings.
```xml
<?xml version="1.0" encoding="utf-8"?>
<resources>
   <string name="remoteAccessConsumerKey">3MVG9Iu66FKeHhINkB1l7xt7kR8czFcCTUhgoA8Ol2Ltf1eYHOU4SqQRSEitYFDUpqRWcoQ2.dBv_a1Dyu5xa</string>
   <string name="oauthRedirectURI">testsfdc:///mobilesdk/detect/oauth/done</string>
   <string-array name="oauthScopes">
       <item>api</item>
   </string-array>
   <string name="androidPushNotificationClientId"></string>
</resources>

```

## Reference
- [Trailhead - Create a React Native App](https://trailhead.salesforce.com/modules/mobile_sdk_react_native/units/mobilesdk_reactnative_create_app)