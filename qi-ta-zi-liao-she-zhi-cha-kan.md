#其它资料设置查看


## 1.查看用户资料
## 2.封禁用户
## [3.用户 关注/取消关注 的逻辑](#follow)
## [4.封禁用户](#block_user)
## [5.私信的收发](#private_message)
***
***
***


## 1.查看用户资料

![](/assets/ScreenShot2018-01-15_15.41.19.png)

## 2.封禁用户
* 1.用管理员在登录的情况下，查看用户的资料，就会看到有 禁封/解禁 的按钮显示
* 2.相关的图片.
![](/assets/ScreenShot2018-01-15_14.01.05.png)
![](/assets/ScreenShot2018-01-16_10.11.00.png)
![](/assets/ScreenShot2018-01-15_14.01.38.png)
![](/assets/ScreenShot2018-01-15_15.41.19.png)

![](/assets/ScreenShot2018-01-15_14.01.38.png)


***

## 3.用户 关注/取消关注 的逻辑<a name="follow"/>
>已经登录了一个用户，然后在其他用户的主目录那里就可以看到 ‘关注/取消关注’

* 1.主要的互动界面在 ```view/default/user.php```
* 2.点击 关注/取消关注 按钮,跳转到 static/js/default/global.js: Manage 中.
    * 1.跳转到 controller/manage.php .
    * 2.转换为 api 模式的返回.
    * 3.取得要 关注/取消关注 的 条目的 id. 
    * 4.取得要返回的 follow / Unfollow 字.
    * 5.返回一个 json ,json 的内容包括 follow/unfollow
    * 3.把返回的 字段 显示出来.

***

## 4.封禁用户<a name="block_user"/>
>管理员 封禁用户 的操作(不能发表新的文章)

* 1.主要的互动界面在 ```view/default/user.php```
* 2.点击 关注/取消关注 按钮,跳转到 static/js/default/global.js: Manage 中.

***

## 5.私信的收发<a name="private_message"/>
* 1.相关的逻辑
    * 1.controller ->  controller/inbox_view.php
    * 2.//通过 私信的 id 和 关联的人的 id ,找到 私信信息
    * 3.view 在 view/default/inbox.php 中.
        * 1.加载私信 MessageList 的详细信息
          * 1.(static/js/default/global.js  ->   loadMoreMessages  ).
          * 2.从 view/api/inbox.php 中取得信息,并以 json 方式返回.
        * 2.

* 相关的截图:
![](/assets/ScreenShot2018-01-16_11.55.28.png)
![](/assets/ScreenShot2018-01-16_11.55.02.png)
![](/assets/ScreenShot2018-01-16_11.54.52.png)






