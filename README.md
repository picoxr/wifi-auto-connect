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

## Functions in Wifi auto connection demo

1.PicoUnityActivity.CallObjectMethod("wifiConnected");Used to check
the state of config.txt flie and start to connect specific Wi-Fi. The result
will be showed in the panel of the scene.

2.PicoUnityActivity.CallObjectMethod <boolean>(ref result,"GetWifiConnectedState");Used to get the state of Wifi connection. If connected, the specified Wifi name will be showed in the panel, or it will show "Connecting". The return value flag:

True：Connected

False：Not connected

