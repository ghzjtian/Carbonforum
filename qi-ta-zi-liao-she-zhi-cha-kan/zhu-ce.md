# 注册


### 1.注册
 * 1.防止攻击的功能，跟登录一样.
 
 
 * 2.登录完成后，就生成一个 6 位数的 Salt.
 * 3.保存到数据库的密码为md5(md5(passwd).salt).
 * 4.注册完成后，就保存 UserID,ExpirationTime,UserCode 到 Cookies.

* 5.相关的算法

```
$TemporaryUserExpirationTime = 30 * 86400 + $TimeStamp;
define('SALT', 'AuthorIsLinCanbin');
$NewUserSalt     = mt_rand(100000, 999999);
//用户的 Password
$NewUserPassword = md5($Password . $NewUserSalt);
//用户的 验证Code 
'UserCode' => md5($NewUserPassword . $NewUserSalt . $TemporaryUserExpirationTime . SALT)

```


### 2.相关的截图
![](/assets/ScreenShot2018-03-21_13.57.35.png)
* 1.注册完成，会以已登录的方式登录到首页
![](/assets/ScreenShot2018-03-21_14.00.10.png)


 



