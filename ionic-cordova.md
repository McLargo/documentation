##  ionic

few useful commands for ionic

#### create new project
`ionic start freshlypressed`

#### run ionic server
`ionic serve`

#### add android platform
`ionic platform add android`

#### add cordova.js and add to body class: platform-android
`ripple emulate`

#### build android APK
`ionic build android`

## with the apk, move to device and install

```
adb push <path>\apk\android-debug.apk /data/local/tmp/<destination_path>`
adb shell pm install -r "/data/local/tmp/<destination_path>"
```

## how to build apk with cordova

```
D: && cd D:\Code\freshlypressed

set ANDROID_HOME=D:\Programs\Android\sdk
set PATH=%PATH%;%ANDROID_HOME%\tools;%ANDROID_HOME%\platform-tools


D: && cd D:\<path>\httpdocs-phonegap
cordova build android
adb push D:\<path>\httpdocs-phonegap\platforms\android\build\outputs\apk\android-debug.apk /data/local/tmp/<destination_path>
adb push android\build\outputs\apk\android-debug.apk /data/local/tmp/<destination_path>
adb shell pm install -r "/data/local/tmp/<destination_path>"

cordova build android && adb push D:\<path>\httpdocs-phonegap\platforms\android\build\outputs\apk\android-debug.apk /data/local/tmp/<destination_path> && adb shell pm install -r "/data/local/tmp/<destination_path>"
```

## addition of permissions to android app

```
<uses-permission android:name="android.permission.RECEIVE_SMS" />
<uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE" />
<uses-permission android:name="android.permission.SET_WALLPAPER" />
<uses-permission android:name="android.permission.DEVICE_POWER" />
```

## validation of jks

```
D:\Programs\Android\sdk\build-tools\25.0.1
apksigner verify --print-certs android.apk


C:\Program Files\Java\jdk1.8.0_121\bin
keytool -list -v -keystore <project>.jks
```

## for ios

```
D: && cd D:\Code\EVACC04\47\Desarrollo\Fuentes\trunk\httpdocs-phonegap

cordova build ios
```


[Install ios sdk](https://cordova.apache.org/docs/es/latest/guide/platforms/ios/index.html#instalar-el-sdk)

