# 忘记密码

### 1.忘记密码
* 1.忘记密码的页面: http://carbon2.com/forgot?
    * 1.1 在验证了来源的正确性和用户名的确存在后，会发送一个邮件到指定的邮箱中.
    * 1.2 AccessToken 的生成方法为: 

```
$AccessToken         = base64_encode($UserName . '|' . $TokenExpirationTime . '|' . md5($UserInfo['Password'] . $UserInfo['Salt'] . md5($TokenExpirationTime) . md5(SALT)));
```
    * 1.3 封装了调用 SMTP 邮件的发送发送的方法.

* 2.邮件中收到的重置密码的链接为: http://carbon2.com/reset_password/Token




