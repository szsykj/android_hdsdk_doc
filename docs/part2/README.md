##注册账号

 ```java
/**
 * 注册账号
 * @param account    邮箱或手机号
 * @param password   密码
 * @param checkCode  验证码
 * @param regionCode 区域代码
 * @param callBack   回调接口
 */
void register(String account, String password, String checkCode, String regionCode, ResultCallBack<UserModel> callBack);
```

##登录账号

```java
/**
 * 登录账号
 * @param account    邮箱或手机号
 * @param password   密码
 * @param regionCode 区域代码
 * @param callBack   回调接口
 */
void login(String account, String password,String regionCode, ResultCallBack<UserModel> callBack);
```

##退出登录

```java
/**
 * 退出登录
 * @param callBack   回调接口
 */
void logout(ResultCallBack callBack);
```

##重置密码

```java
/**
 * 重置密码
 * @param account   邮箱或手机号
 * @param password  密码
 * @param checkCode 验证码
 * @param callBack  回调接口
 */
void resetPassword(String account, String password, String checkCode,ResultCallBack callBack);
```

##获取验证码

```java
/**
 * 获取验证码
* @param checkType CHECK_REGISTER 注册验证码
*                  CHECK_FORGET   忘记密码验证码
*                  CHECK_LOGIN    登录验证码
 * @param callBack  回调接口
 */
void getAccountCheckCode(String account, CheckType checkType, ResultCallBack callBack);
```

##更新用户名称

```java
/**
 * 更新用户名称
 * @param name     用户名称
 * @param callBack 回调接口
 */
void updateUserName(String name, ResultCallBack callBack);
```

##更新用户头像

```java
/**
 * 更新用户头像
 * @param file     头像图片文件
 * @param callBack 回调结果
 */
void updateUserIcon(File file, ResultCallBack callBack);
```

##更新用户密码

```java
/**
 * 更新用户密码
 * @param oldPassword 用户旧密码
 * @param password    用户新密码
 * @param callBack    回调结果
 */
void updateUserPassword(String oldPassword,String password,ResultCallBack callBack);
a```

##UserModel数据模型
| 字段名称          | 类型  | 字段说明   |
|---------------|-----|--------|
| userId        | 数字  | 用户id   |
| email         | 字符串 | 邮箱     |
| userName      | 字符串 | 用户名称   |
| createTime    | 数字  | 创建时间   |
| iconUrl       | 字符串 | 用户头像地址 |
| phone         | 字符串 | 手机号码   |
| hasCreateHome | 数字  | 是否创建家庭 |

##FeedbackBean数据反馈模型
| 字段名称            | 类型  | 字段说明                   |
|-----------------|-----|------------------------|
| feedbacId       | 数字  | 反馈ID                   |
| createTime      | 数字  | 添加时间                   |
| feedbackStatus  | 数字  | 反馈状态；0：未处理，1：已处理，2：处理中 |
| feedbackContent | 字符串 | 反馈内容                   |
| systemReply     | 字符串 | 系统反馈                   |
