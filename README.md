# WIFI自动连接功能解决方案

新建Unity工程，把Demo中的Plugins->Android中的Picovr_WifiManager_version.jar包，拷贝到Unity工程对应的目录下。将Demo中的PicoUnityActivity.cs脚本拷贝到Unity工程任意目录下

## AndroidManifest文件修改

1.增加**android:sharedUserId="android.uid.system"**必须系统签名

2.加入网络相关权限，如下图所示。

3.修改MainActivity

## 配置文件说明

1.配置文件存放位置应为系统pre_resource/config/**目录下（需在pre_resource目录下新建一个config文件夹），如希望指定为其他目录，则需要修改Jar包中代码。

2.配置文件格式，如下图所示。ssid后填写WIFI名，pswd后填写WIFI密码。

   注：WIFI名称请使用英文字符

## 接口说明

1.PicoUnityActivity.CallObjectMethod("wifiConnected");判断配置文件并开始连接

2.PicoUnityActivity.CallObjectMethod <boolean>(ref result,"GetWifiConnectedState");
