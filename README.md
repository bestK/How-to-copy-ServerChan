# How-to-copy-ServerChan

Server酱」，英文名「ServerChan」，是一款「程序员」和「服务器」之间的通信软件。 

说人话？就是从服务器推报警和日志到手机的工具。http://sc.ftqq.com 这是她的地址

![ServerChan](http://anime-img.stor.sinaapp.com/55ec21e37e46b.gif)



介绍是从官方复制过来，下面我们来分析一下项目可行性。看下图

## route
```
+-----------+        +-----------+         +-------------+          +------------------+        +--------------+
|           |        |           |         | qrcode      |          |                  |        |              |
| account   +------->+  key      +-------->+             +--------->+  getOpenidByKey  +------->+  push msg    |
|           |        |           |         | key         |          |                  |        |              |
+-----------+        +-----------+         +-------------+          +------------------+        +--------------+

```


### Account

客户端注册账户以便生成 `key` ，可手动注册，或引入第三方帐号。如: Github、Sina、QQ等。

### Key

为账户生成一个唯一不重复的 `key` 

### QrCode

通过 `key` 生成场景微信关注二维码，后续可以根据这个唯一绝对不重复的 `key` 获得对应的关注用户的 `openId`.

### getOpenidByKey

当用户构造一个类似 [https://example.com/push_msg?key=8888888888](#) 的请求时，我们的程序应该如下处理：

... 

略掉好了，我就不信你不知道


###  push msg

略.



---
别忘了，这一切都要从拥有一个微信公众号开始。 [微信公众平台接口测试帐号申请](http://mp.weixin.qq.com/debug/cgi-bin/sandbox?t=sandbox/login)
