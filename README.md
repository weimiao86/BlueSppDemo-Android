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
## Creat the UI

* In the **Component Tree** section, convert the **ConstrainLayout** to **RelativeLayout**.

* Add the components to the **activity_main.xml**:
```
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <requestFocus />

    <TextView
        android:id="@+id/textStatus"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_alignParentTop="true"
        android:layout_centerHorizontal="true"
        android:text="@string/bt_notConnected"
        android:textSize="12sp" />

    <LinearLayout
        android:id="@+id/layout1"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_alignParentBottom="true"
        android:orientation="horizontal"
        android:layout_centerHorizontal="true" >

        <EditText
            android:id="@+id/etMessage"
            android:layout_width="0dp"
            android:layout_height="wrap_content"
            android:layout_gravity="bottom"
            android:layout_weight="1"
            android:ems="10"
            android:hint="@string/bt_write"
            android:inputType="none" />

        <Button
            android:id="@+id/btnSend"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="@string/bt_send" />
    </LinearLayout>

    <ScrollView
        android:id="@+id/scrollView1"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:layout_above="@+id/layout1"
        android:layout_below="@id/textStatus"
        android:layout_alignParentStart="true"
        android:layout_alignParentEnd="true">

        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:orientation="vertical" >

            <TextView
                android:id="@+id/textRead"
                android:layout_width="match_parent"
                android:layout_height="match_parent"
                android:text="@string/bt_received"
                android:textSize="16sp" />

        </LinearLayout>
    </ScrollView>

</RelativeLayout>
```

* Edit the **strings.xml**:
```
<resources>
    <string name="app_name">BlueSppDemo</string>
    <string name="bt_connect">Connect</string>
    <string name="bt_send">Send</string>
    <string name="bt_notConnected">"Status: Not connect</string>
    <string name="bt_received">Received data</string>
    <string name="bt_write">type command here</string>
    <string name="action_settings">Settings</string>
</resources>
```


