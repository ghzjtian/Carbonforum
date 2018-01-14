#主入口_index.php文件

### [1.路由模式](#route_mode)
### [2.进入用户目录.](#user_directory)
### [3.View 的分发](#view_dispatch)
***
***
***

### 1.路由模式<a name="route_mode"/>
* 1.$Routes 根据传入的参数的不同，进入不同的文件.

***

### 2.进入用户目录.<a name="user_directory"/>
* 1.如果 $UserName 为数字,则重新定向到指定的用户 id 的用户目录中.

* 2.相关图片
    * 1.用户主目录
    ![](/assets/ScreenShot2018-01-14_11.00.41.png)
    * 2.没有此用户
    ![](/assets/ScreenShot2018-01-14_11.09.45.png)
    
***

### 3.View 的分发<a name="view_dispatch"/>
* 1.都是在 view/default/layout.php (头和底的模板显示)上的显示,其中的 $ContentFile 则是可以根据业务区变化的.
    