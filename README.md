# WeChatPush
利用微信公众平台测试号进行消息推送的bash脚本

## 微信公众平台接口测试账号操作

[申请测试号的地址 https://mp.weixin.qq.com/debug/cgi-bin/sandbox?t=sandbox/login](https://mp.weixin.qq.com/debug/cgi-bin/sandbox?t=sandbox/login)  

手机扫描登录公众平台测试号

找到`测试号信息`，记住`appid`和`appsecret`，一会儿会用到    

找到`新增测试模板`，添加模板消息    

填写模板标题`服务器状态报告`，填写如下模板内容    
``` conf
来自{{Source.DATA}}的{{Type.DATA}}：
{{Overview.DATA}}

详细信息：
{{Details.DATA}}
```
提交保存之后，记住该`模板ID`，一会儿会用到    

找到`测试号二维码`。手机扫描此二维码，关注之后，你的昵称会出现在右侧列表里，记住该微信号，一会儿会用到（注：此微信号非你真实的微信号）    

## 发送微信模板消息

**修改配置文件中WeChat开头的4个变量，请看注释**    

## 测试程序

在Linux上执行程序

wechatpush -e

在手机上查看，已经收到了内置的测试消息    
