#用户注册及登录

##[1.注册](#register)

##[2.登录](#login)


***
***
***


##1.注册<a name="register"/>

* 1.控制器(处理登录的逻辑):
```controller/register.php```
* 2.View:
    * 1.内容:view/default/register.php
    * 2.其它布局:view/default/layout.php

    * 4.输入框的判断：用 javascript 检查输入框那里是否输入正确，数据库是否已经有了一样的名字.
    * 5.生成随机的 盐值 并保存.
    * 6.注册完成后，直接登录.(记住了 $CurUserID)
    * 7.第一个注册的人为管理员.
    * 8.生成头像
    * 9.保存 cookie.
    
* 3.相关的图片
    * 1.输入的名字已经有了(javascript的检查)
![](/assets/ScreenShot2018-01-14_23.25.13.png)
    * 2.输入的名字已经有了(点击注册)
![](/assets/ScreenShot2018-01-14_23.26.11.png)
    * 3.数据库的结构
    ![](/assets/ScreenShot2018-01-15_10.00.49.png)
    ![](/assets/ScreenShot2018-01-15_10.00.20.png)

***

##2.登录<a name="login"/>

* 1.控制器(处理登录的逻辑):
```controller/login.php```
* 2.View:
    * 1.内容:view/default/login.php
    * 2.其它布局:view/default/layout.php
    * 3.保存 cookie.
    
    
* 3.相关的图片:
    * 1.登录
    ![](/assets/ScreenShot2018-01-14_16.57.32.png)
    * 2.cookie 的存储
    ![](/assets/ScreenShot2018-01-14_18.46.50.png)
    