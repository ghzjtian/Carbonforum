#手机版APP



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
>从 DB carbon_topics 中获取数据.
    * 3.格式化 view/api/home.php
    * 4.输出 view/api/layout.php
    
    
***

### 2.点击某个文章，跳进文章的详细页面
    * 1.POST 方法: https://api.94cb.com/t/3434-1
    * 2.header , Content-Type : application/x-www-form-urlencoded
    * 3.参数: SKey=12450&STime=1516350991&SValue=3392b9e09f968dc7f0eb3ef2e1867936

####2.1服务器流程:
    * 2.跳转到 控制器 /index.php -> /controller/topic.php
>获取数据.
    * 3.格式化 view/api/home.php
    * 4.输出 view/api/layout.php







