#手机版APP

###1.判断来源请求是否是来自 APP ：
>$IsApp = $_SERVER['HTTP_HOST'] == $Config['AppDomainName'] ? true : false;


### 1.首页获取 Topics 的列表数据

    * 1.POST 方法: https://api.94cb.com/page/1
    * 2.header , Content-Type : application/x-www-form-urlencoded
    * 3.参数: SKey=12450&STime=1516350991&SValue=3392b9e09f968dc7f0eb3ef2e1867936