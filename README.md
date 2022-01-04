# react-native-android-wake-screen

Fork of https://github.com/witPranav/react-native-android-wake-screen that works with gradle 7.

## Getting started

`$ npm install @satankebab/react-native-android-wake-screen --save`

### Mostly automatic installation

`$ react-native link @satankebab/react-native-android-wake-screen`

## Usage
This module helps turn the screen display on from within a headless function.

Add the following inside the project manifest (android/app/src/main/AndroidManifest.xml):
```xml
<uses-permission android:name="android.permission.WAKE_LOCK" />   //Add this line
<application
      android:name=".MainApplication"
      android:label="@string/app_name"
      android:icon="@mipmap/ic_launcher"
      android:roundIcon="@mipmap/ic_launcher_round"
      android:allowBackup="false"
      android:turnScreenOn="true"                          // Add this line
      android:theme="@style/AppTheme">
```

```javascript
import AndroidWakeScreen from '@satankebab/react-native-android-wake-screen';

//inside your headless function
const MyHeadlessFunction = async () => {
  AndroidWakeScreen.wakeScreen();
};
```
