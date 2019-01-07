# Method of Wi-Fi Auto Connection

Copy Picovr_WifiManager_version.jar
and PicoUnityActivity.cs into your project, and make sure Picovr_WifiManager_version.jar
is under path Assets/Plugins/Android/

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

# WIFI自动连接功能解决方案

新建Unity工程，把Demo中的Plugins->Android中的Picovr_WifiManager_version.jar包，拷贝到Unity工程对应的目录下。将Demo中的PicoUnityActivity.cs脚本拷贝到Unity工程任意目录下

## AndroidManifest文件修改

1.增加**android:sharedUserId="android.uid.system"**必须系统签名
![](https://github.com/PicoSupport/PicoVRWifimanager/blob/master/assets/01.png)

2.加入网络相关权限，如下图所示

![](https://github.com/PicoSupport/PicoVRWifimanager/blob/master/assets/02.png)

3.修改MainActivity
![](https://github.com/PicoSupport/PicoVRWifimanager/blob/master/assets/03.png)

## 配置文件说明

1.配置文件存放位置应为系统pre_resource/config/**目录下（需在pre_resource目录下新建一个config文件夹），如希望指定为其他目录，则需要修改Jar包中代码。

2.配置文件格式，如下图所示。ssid后填写WIFI名，pswd后填写WIFI密码。

   注：WIFI名称请使用英文字符
   
   ![](https://github.com/PicoSupport/PicoVRWifimanager/blob/master/assets/04.png)

## 接口说明

1.PicoUnityActivity.CallObjectMethod("wifiConnected");判断配置文件并开始连接

2.PicoUnityActivity.CallObjectMethod <boolean>(ref result,"GetWifiConnectedState");
