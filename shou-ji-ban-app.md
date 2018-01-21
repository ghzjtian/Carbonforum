#手机版APP

### 1.首页获取 Topics 的列表数据
### 2.点击某个文章，跳进文章的详细页面


***
***
***

### 1.首页获取 Topics 的列表数据

    * 1.POST 方法: https://api.94cb.com/page/1
    * 2.header , Content-Type : application/x-www-form-urlencoded
    * 3.参数: SKey=12450&STime=1516350991&SValue=3392b9e09f968dc7f0eb3ef2e1867936
    
####1.1服务器流程:
    * 1.判断为 APP 模式请求: /common.php 
>$IsApp = $_SERVER['HTTP_HOST'] == $Config['AppDomainName'] ? true : false;

    * 2.跳转到 控制器 /index.php -> /controller/home.php
>从 DB carbon_topics 中获取列表数据.
    * 3.格式化 view/api/home.php
    * 4.输出 view/api/layout.php
    
    
***

### 2.点击某个文章，跳进文章的详细页面
    * 1.POST 方法: https://api.94cb.com/t/3434-1
    * 2.header , Content-Type : application/x-www-form-urlencoded
    * 3.参数: SKey=12450&STime=1516350991&SValue=3392b9e09f968dc7f0eb3ef2e1867936

####2.1服务器流程:
    * 2.跳转到 控制器 /index.php -> /controller/topic.php
>1.从 DB carbon_topics 中获取特定 ID 的 Topic 数据（判断该 Topic 是否存在）
>2.根据 Topic ID 在 carbon_posts 中获取该 Topic 的详细的资料.
>3.获取该 Topic ID 是否已经被当前用户添加为 Favourite
>4.更新该 Topic ID 在 DB carbon_topics 中的 浏览量
    * 3.格式化 view/api/topic.php
    * 4.输出 view/api/layout.php


***

### 3.回复文章或留言

* 1.APP 点击 某个文章或留言 的回复按钮 , 跳转到 ReplyActivity
.

* 2.点击 发送 按钮，发送文章的回复.
>intent.putExtra("TopicID", mTopicID);
>intent.putExtra("Content", contentHTML);

* 3.ReplyService 回复发送中:
    * 1.弹出 Notification 提示 回复发送中.
    * 2.上传 回复信息








