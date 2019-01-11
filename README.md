[Call And Export Jar Package](https://github.com/PicoSupport/PicoSupport/blob/master/Call%20And%20Export%20Jar.docx)<p align="right"><a href="https://github.com/PicoSupport/PicoSupport" target="_blank"> <img src="https://github.com/PicoSupport/PicoSupport/blob/master/Assets/home.png" width="20"/> </a></p>

# Method of Wi-Fi Auto Connection

Create a new Unity project and copy the Picovr_WifiManager_version. Jar package in assets into the corresponding directory of plugins-> Android in Unity project.Copy the picounityactivity.cs script from assets into any directory of the Unity project

## Modify AndroidManifest

1.Add shared user id in the script. android:sharedUserId="android.uid.system"

![](https://github.com/PicoSupport/PicoVRWifimanager/blob/master/assets/01.png)

2.Add permissions related to network, see the picture below.

![](https://github.com/PicoSupport/PicoVRWifimanager/blob/master/assets/02.png)

3.Modify the name of mainactivity

![](https://github.com/PicoSupport/PicoVRWifimanager/blob/master/assets/03.png)

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

