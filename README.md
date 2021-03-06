# zzpay
ZZPay - 开源个人收款系统，支持支付宝、微信收款码，资金直接到达本人账号，免签通道个人移动端自动回调，不需提现，不需备案，完全免费，个人收款0风险方案。

# ZZPay - 开源个人收款系统


### ZZPay是基于php + mysql 实现的一套免签支付程序，主要包含以下功能：
- 收款即时到账，无需进入第三方账户，收款更安全
- **服务端和安卓监控端全部开源，无后门更安全，二次开发方便**
- 超简单Api使用，提供统一Api实现收款回调
- 提供示例代码简单接入
- 免root，免xp框架，不修改支付宝/微信客户端，防封更安全
- 支持监听店员收款信息，可使用支付宝微信小号/模拟器挂机  

### 声明
> 1.本服务内容是指ZZpay通过合法的互联网技术，向个人用户提供支付宝 & 微信即时到账提醒的业务。

> 2.本服务允许个人商业化使用。 


> 3.本服务严禁用于违反中国互联网管理条例中任何一条有关危害互联网安全、侵犯他人知识产权等的违法行为。

### 本项目运行Demo

- 电脑端进入→ [在线demo](http://zzpay.zz82.net/) 


###  个人申请支付接口现状
- 原生支付宝，微信支付

    - >支付宝微信只服务于有营业执照、个体工商户的商户。截止目前（2019-01-01）无法以个人身份（或以个人为主体）直接申请API。
      >结论：不可行结论：不可行

- 关联企业支付宝账号

    - >即新建企业账户，然后采用已经实名认证了的企业账户关联该账户，用其实名主体完成新账户的实名认证。一系列操作完成后，新的账户具有和企业账户一样的资质可以申请API。

      >结论：如果条件允许，推荐此方案

- 聚合支付工具，Ping++等


    - >就是个第四方聚合支付工具，简化了接入开发流程而已，个人开发者仍然需要去申请所需接口的使用权限。

      > 结论：不可行

- 第四方聚合支付

    - >支付资金进入官方账号，自己再进行提现操作。需要开通域名，提现手续费较高，支付页面不支持自定义。另外，对于此种类型的聚合支付平台，隐藏着极高的跑路风险。

      >结论：不推荐

- 有赞

    - >通过有赞微商城支付接口收款。

      >结论：不推荐，需手动提现，不免费，费用6800/年起，一旦风控资金很难取出。

- 利用拼多多店铺、淘宝代付功能等

    - >结论：不推荐，可能随时被风控。

- 挂机监听软件，PaysApi、绿点支付等


    - >采用挂机监听的策略

      >结论：第三方平台，存在安全隐患，成本高，费率高，不免费

- 其他基于Xposed挂机监听软件

    - >基于virtual xposed hook相关技术，可自动生成任意备注金额收款码 参考抢红包外挂

      >结论：成本高，配置麻烦，需24小时挂台安卓手机，量大易触发风控、不免费，黑产适用

- Payjs （疑使用[微信小微商户](https://pay.weixin.qq.com/index.php/core/affiliate/micro_intro)）

    - >结论：仅支持微信、不免费、使用官方接口收取代开费用

- 国外支付，PayPal、Strip：不可用

### ZZPay个人收款支付系统

>支持支付宝、微信收款码，资金直接到达本人账号，免签通道个人移动端自动回调，不需提现，不需备案，完全免费，个人收款0风险方案。

>**服务端和安卓监控端全部开源，无后门更安全，二次开发方便**

### 流程原理（24小时自动回调）

- 原理说明

`第一步：用户在你的网站点击购买 -> 向你的zzpay_server 发起支付订单 ->`

`第二步：zzpay_server 返回你的二维码 -> 用户扫码支付 -> 钱到你的微信/支付宝 -> zzpay_app 监听到钱支付成功 ->`

`第三步：zzpay_app 告诉zzpay_server 这个支付成功的消息 -> zzpay_server 把这个消息回调给你的网站(notify_url)`

- 支付流程图
    ![](http://zzpay.zz82.net/img/flowchart.png)


#### ZZPay源码（含详细文档）获取方式 
- 进入 [ZZPay官网](http://zzpay.zz82.net/) 成功支付测试后，将自动发至你所填写的邮箱中

### 技术疑问交流
- 进入 [ZZPay官网](http://zzpay.zz82.net/) ，可获取各项目详细图文文档、疑问解答
