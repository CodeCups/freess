
现在翻墙越来难度越大了。 不过 ，想翻墙还是有办法的，比如使用shadowsocks实现科学上网。

#### shadowsocks翻墙的原理

shadowsocks是一款自定义协议的代理软件，由于其流量特征不明显，不太容易用技术手段拦截。虽然作者@clowwindy两年前就被有司请喝茶了，shadowsocks却一直运转良好没有被彻底封杀过。

shadowsocks客户端启动后会在本地开启一个代理，可以理解为一个数据的出入口。用户想通过shadowsocks访问墙外网站的请求都要经过这个本地代理。

<!-- more --> 

#### shadowsocks翻墙上网的过程

1. 用户发起一个网络访问请求，比如用浏览器访问google.com，请求被发送到本地代理。

1. 客户端从本地代理拿到请求数据，然后发送至墙外的shadowsocks服务端。

1. 服务端向google.com发起请求，然后收到google的响应数据，也就是google首页的数据。

1. 服务端把响应数据发回客户端。

1. 客户端再通过本地代理把响应数据交给浏览器，google首页就显示出来了。

整个过程中的第2步和第4步都是通过shadowsocks自定义的协议隐蔽地进行，很难被过滤，所以我们才能一直用它顺畅地翻墙。

#### 简单地说，用shadowsocks翻墙，你需要一个客户端和一个服务端。

##### 客户端

[Windows](https://github.com/shadowsocks/shadowsocks-windows/releases)、[macOS](https://github.com/shadowsocks/ShadowsocksX-NG/releases)、[Android](https://github.com/shadowsocks/shadowsocks-android/releases)平台都有官方提供的免费客户端可用，下载地址如下：

[Windows](https://github.com/shadowsocks/shadowsocks-windows/releases)

[macOS](https://github.com/shadowsocks/ShadowsocksX-NG/releases)

[Android](https://github.com/shadowsocks/shadowsocks-android/releases)

iOS平台有一些收费的App支持shadowsocks, 比如

[shadowrocket](https://itunes.apple.com/us/app/shadowrocket/id932747118?mt=8&utm_source=textarea.com&utm_medium=textarea.com&utm_campaign=article)

#### shadowsocks服务端购买
市面上有一些shadowsocks服务可供购买，比如


[掠影](https://www.sstz.info) https://www.sstz.info/

如果你愿意折腾，可以自己租一个VPS搭建shadowsocks服务，成本更低，而且流量上限取决于你购买的VPS套餐，一般来说都很充裕。



#### 配置shadowsocks客户端
客户端和服务端都有了，只要配置一下客户端就可以愉快地翻墙了。

客户端需要按照服务器的配置填写服务器IP地址、服务器端口、本地端口（如果没有本地端口选项，就是默认的1080）、密码、加密方式等参数，可以参看上面的“编写配置文件”小节。
客户端
- [Windows](https://github.com/shadowsocks/shadowsocks-windows/wiki/Shadowsocks-Windows-%E4%BD%BF%E7%94%A8%E8%AF%B4%E6%98%8E) / [OS X](https://github.com/shadowsocks/shadowsocks-iOS/wiki/Shadowsocks-for-OSX-Help)
- [Android](https://github.com/shadowsocks/shadowsocks-android) / [iOS](https://github.com/shadowsocks/shadowsocks-iOS/wiki/Help)
- [OpenWRT](https://github.com/shadowsocks/openwrt-shadowsocks)

#### 免费shadowsocks账号在这里

```
{
  "server" : "sgp.sstz.info",
  "server_port" : 49949,
  "method" : "aes-256-gcm",
  "password" : "sstz.info",
}
```





