# BlueSppDemo-Android

This is a demo of how to use the [Android-BluetoothSPPLibrary](https://github.com/akexorcist/Android-BluetoothSPPLibrary) in Android Studio 3.1.1

## Usage

* To get started, create a new project in the android studio with an Empty Activity template, set the Min API level to 18.

* Under **Gradle Scripts** --> **build.gradle(Module:app)**, append the line **implementation 'com.akexorcist:bluetoothspp:1.0.0'** to the end of **dependencies**.
```
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


