##集成SDK
本章介绍如何集成SDK,请使用Android studio编辑器来开发


##创建工程
在Android Studio中建立你的工程，并在libs文件夹中添加SmartHomeSDK_HD_v1.0.0.jar文件。


## build.gradle 配置
build.gradle 文件里添加集成准备中下载的dependencies 依赖库。  
```java
implementation 'com.google.code.gson:gson:2.8.5'
implementation files('libs\\sdk.jar')
```

## AndroidManifest.xml 配置
在Androidmanifest中添加以下权限及服务
```java
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
<uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE" />
<uses-permission android:name="android.permission.ACCESS_WIFI_STATE" />
<uses-permission android:name="android.permission.ACCESS_COARSE_LOCATION" />
<uses-permission android:name="android.permission.ACCESS_FINE_LOCATION" />
```

##SDK初始化
在application中初始化sdk后，使用sdk中对外提供的接口(具体接口使用参考demo实例)
```java
public class DemoApplication extends Application {
    @Override
    public void onCreate() {
        super.onCreate();
        SYSdk.init(this);
    }
}
```

