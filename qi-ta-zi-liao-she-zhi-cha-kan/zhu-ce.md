# 注册


### 1.注册
 * 1.防止攻击的功能，跟登录一样.
 
 
 * 2.登录完成后，就生成一个 6 位数的 Salt.
 * 3.保存到数据库的密码为md5(md5(passwd).salt).
 * 4.注册完成后，就保存 UserID,ExpirationTime,UserCode 到 Cookies.



### 2.相关的截图
![](/assets/ScreenShot2018-03-21_13.57.35.png)



 



