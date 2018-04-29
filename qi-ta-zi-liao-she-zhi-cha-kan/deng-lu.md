# 登录


###1.登录
###2.登录后保存的 cookie


***
***
***

###1.登录
#####* 1.在 name 框中，onblur 检测用户名是否已经存在.
#####* 2.# 登录操作
* 2.1.FormHash : 表单校验散列.(校验的方法为 ```substr(md5($Config['SiteName'] . SALT), 8, 8)```,如 SiteName 为 'Carbon Forum', SALT 为 AuthorIsLinCanbin , 则得到的结果为 2b797703c5ff8004360787639da7779b,从第 8 位开始，取 8 位，则为 c5ff8004).注意,这个可以在浏览器的查看源码中看到!!!
* 2.2.在 ```controller/login``` 中，会验证 ```($_SERVER['HTTP_REFERER'])``` 和 ```$_SERVER['HTTP_HOST']``` 的主机名是否相同的，如果不相同，就会触发 403 ,防止攻击的功能.
>HTTP_HOST    localhost 
HTTP_REFERER    http://localhost/ 
>
>'HTTP_REFERER'
引导用户代理到当前页的前一页的地址（如果存在）。由 user agent 设置决定。并不是所有的用户代理都会设置该项，有的还提供了修改 HTTP_REFERER 的功能。简言之，该值并不可信。
>'HTTP_HOST'
当前请求头中 Host: 项的内容，如果存在的话。


* 2.3  登录完成后，就保存 UserID,ExpirationTime,UserCode 到 Cookies.



***

###2.登录后保存的 cookie
* 1.图片
![](/assets/ScreenShot2018-03-20_10.44.58.png)
