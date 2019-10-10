
#设备分享


##获取某个设备被分享的用户列表
```java
/**
* 获取分享的用户列表
*
* @param did            设备的did
* @param resultCallBack 回调接口
*/
void getDeviceSharedList(int did, ResultCallBack<List<ShareItemBean>> resultCallBack);
```

##用户查看家庭中分享出去的设备
```java
/**
 * 用户查看家庭中分享出去的设备
 *
 * @param hid            家庭id
 * @param resultCallBack 回调接口
 */
void getHomeShareDeviceList(int hid, final ResultCallBack<SharedDeviceResult> resultCallBack);
```


##分享一个设备给某个用户
```java
/**
* 分享设备给用户
* @param did 要分享的设备id
* @param account 要分享给的账号
* @param resultCallBack 回调接口
*/
void shareDeviceToUser(int did, String account, ResultCallBack resultCallBack);
```

##移除分享
```java
/**
* 移除分享
* @param shareItemBean 要删除的item
* @param resultCallBack 回调
*/
void removeDeviceShare(ShareItemBean shareItemBean, ResultCallBack resultCallBack);
```



#ShareItemBean 数据模型

| 字段名称              | 字段说明   | 类型  | 备注        |
|-------------------|--------|-----|-----------|
| userId            | 用户id   | 数字  | \-        |
| nudId             | 用户设备Id | 数字  | \-        |
| userName          | 用户名    | 字符串 | \-        |
| userAccountNumber | 用户账号   | 字符串 | 分为：手机号和邮箱 |
| iconUrl           | 用户头像地址 | 字符串 | \-        |

