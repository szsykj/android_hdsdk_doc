##初始化sigMesh

```java
/**
 * 初始化sigMesh
 * @param context
 */
void init(Context context);
```

##自动连接

```java
/**
 * 自动连接
 * @param update 是否数据更新
 */
void autoConnect(boolean update);
```

##扫描蓝牙ble设备

```java
/**
 * 扫描蓝牙ble设备
 * @param scanParameter         扫描参数
 * @param bleDeviceScanCallBack 设备返回
 */
void startScan(ScanParameter scanParameter, AdvDeviceScanCallBackbleDeviceScanCallBack);
```


##停止蓝牙扫描

```java
/**
 * 停止蓝牙扫描
 */
void stopScan();
```

##开始配置设备mesh网络

```java
/**
 * 开始配置设备mesh网络
 * @param deviceList 配网设备集合
 * @param parameter  配网参数
 * @param callback   结果返回
 */
void startMeshActivate(List<SigMeshDevice> deviceList,MeshActivateParameter parameter, MeshActivateCallBack callback);
```

##结束配置

```java
/*
 * 结束配置
 */
void stopMeshActivate();
```

##删除设备

```java
/**
 * 删除设备
 * @param address 设备mesh地址
 * @param callBack 
 */
void deleteDevice(int address, ResultCallBack callBack);
```

##发送控制指令

```java
/**
 * 发送控制指令
 * @param parameter 指令参数
 * @param callBack  结果返回
 */
void controlCommand(MeshCommandParameter parameter, ResultCallBackcallBack);
```

##开始升级

```java
/**
 * 开始升级
 * @param mac      设备地址
 * @param firmware 固件包
 * @param callBack 结果返回
 */
void startOTA(String mac, byte[] firmware, MeshOTACallBack callBack);
```

##设置sigMesh状态改变监听

```java
/**
 * 设置sigMesh状态改变监听
 * @param listener sigMesh状态改变监听
 */
void registerSigMeshStatusListener(OnSigMeshStatusListener listener);
```

##设置sigMesh状态改变监听

```java
    /**
     * 设置sigMesh状态改变监听
     * @param listener sigMesh状态改变监听
     */
    void unRegisterSigMeshStatusListener(OnSigMeshStatusListener listener);
```

