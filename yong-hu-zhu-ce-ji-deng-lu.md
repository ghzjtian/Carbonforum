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
    * 3.保存 cookie.
    * 4.输入框的判断：用 javascript 检查输入框那里是否输入正确，数据库是否已经有了一样的名字.
    
* 3.相关的图片
![](/assets/ScreenShot2018-01-14_23.25.13.png)


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
    