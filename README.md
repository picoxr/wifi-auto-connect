# Method of Wi-Fi Auto Connection

Note: Regarding JAR file creation and usage, please refer to [the Guideline](https://github.com/PicoSupport/PicoSupport/blob/master/How_to_use_JAR_file_in_Unity_project_on_Pico_device.docx)

## Modify AndroidManifest

1.Add shared user id in the script. android:sharedUserId="android.uid.system"

![](https://github.com/PicoSupport/PicoVRWifimanager/blob/master/assets/01.png)

2.Add permissions related to network, see the picture below.

![](https://github.com/PicoSupport/PicoVRWifimanager/blob/master/assets/02.png)

## Class Name
```
com.picovr.wifimanager.WifiManagerActivity
```

## Instructions of config.txt file

1.The file should under path pre_resource/config/ in the system(create one if the path not exist).

2.About the format of the file please see the picture below. Fill in Wifi name for ssid, and password for pswd.

![](https://github.com/PicoSupport/PicoVRWifimanager/blob/master/assets/04.png)

## Interface
```
 String wifiConnected（）
 bool GetWifiConnectedState（）
```

