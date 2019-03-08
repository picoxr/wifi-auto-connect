# Method of Wi-Fi Auto Connection

Note: Regarding JAR file creation and usage, please refer to [the Guideline](https://github.com/picoxr/support/blob/master/How%20to%20Use%20JAR%20file%20in%20Unity%20project%20on%20Pico%20Device.docx)

## Modify AndroidManifest

1.Add shared user id in the script. android:sharedUserId="android.uid.system"

![](https://github.com/picoxr/PicoWifiManager/blob/master/assets/01.png)

2.Add permissions related to network, see the picture below.

![](https://github.com/picoxr/PicoWifiManager/blob/master/assets/02.png)

## Class Name
```
com.picovr.wifimanager.WifiManagerActivity
```

## Instructions of config.txt file

1.The file should under path pre_resource/config/ in the system(create one if the path not exist).

2.About the format of the file please see the picture below. Fill in Wifi name for ssid, and password for pswd.

![](https://github.com/picoxr/PicoWifiManager/blob/master/assets/04.png)

## Interface
```
 String wifiConnected（）
 bool GetWifiConnectedState（）
```

