# BlueSppDemo-Android

This is a demo of how to use the [Android-BluetoothSPPLibrary](https://github.com/akexorcist/Android-BluetoothSPPLibrary) in Android Studio 3.1.1

## Usage

* To get started, create a new project in the android studio with an Empty Activity template, set the Min API level to 18.

* Under **Gradle Scripts** --> **build.gradle(Module:app)**, append the line **implementation 'com.akexorcist:bluetoothspp:1.0.0'** to the end of **dependencies**.
```gradle
  dependencies {
    implementation fileTree(dir: 'libs', include: ['*.jar'])
    implementation 'com.android.support:appcompat-v7:27.1.1'
    implementation 'com.android.support.constraint:constraint-layout:1.0.2'
    testImplementation 'junit:junit:4.12'
    androidTestImplementation 'com.android.support.test:runner:1.0.1'
    androidTestImplementation 'com.android.support.test.espresso:espresso-core:3.0.1'
    implementation 'com.akexorcist:bluetoothspp:1.0.0'
  }
```

* Declare permission for library: add the two lines below to the **manifests** --> **AndroidManifest.xml**,  

```xml
<uses-permission android:name="android.permission.BLUETOOTH" />
<uses-permission android:name="android.permission.BLUETOOTH_ADMIN" />
```
* The **AndroidManifest.xml** should look like as below:
```xml
<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    package="com.example.wei.bluesppdemo">

    <uses-permission android:name="android.permission.BLUETOOTH"/>
    <uses-permission android:name="android.permission.BLUETOOTH_ADMIN"/>

    <application
        android:allowBackup="true"
        android:icon="@mipmap/ic_launcher"
        android:label="@string/app_name"
        android:roundIcon="@mipmap/ic_launcher_round"
        android:supportsRtl="true"
        android:theme="@style/AppTheme">
        <activity android:name=".MainActivity">
            <intent-filter>
                <action android:name="android.intent.action.MAIN" />

                <category android:name="android.intent.category.LAUNCHER" />
            </intent-filter>
        </activity>
    </application>

</manifest>
```

### You are ready to go, for the detail explaination of the java code, prelase refer to the [Simple Usage](https://github.com/akexorcist/Android-BluetoothSPPLibrary/blob/master/README.md#simple-usage)

