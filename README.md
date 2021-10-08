# Mirai-Linux

> Mirai-QQ 机器人库

* 机器人账号： 2088667670
* 机器人密码： 89765260239qaz
* 测试QQ群号： 519175451

*以下只用作记录测试过程*

---
<details>
<summary>一、Windows测试环境搭建</summary>

## 一、Windows测试环境搭建

### 1. 配置java环境

需要java11版本以上

本次测试使用Java SE Development Kit 11.0.12

https://www.oracle.com/java/technologies/downloads/#java11-windows

### 2. 运行MCL启动器

运行 `mcl-installer-1.0.3-windows-amd64.exe`

根据情况选择安装内容，按传完成后运行 `mcl.cmd` ，运行成功会有 `I/main: mirai-console started successfully.` 提示。

在 `mcl.cmd` 中使用 `login 2088667670 89765260239qaz` 登陆账号。

接下来会提示需要使用 **腾讯验证码助手的在线服务** ，请看 https://txhelper.glitch.me/。

注意，官方提供的在线服务需要安装 **安卓版本** 的APK文件，即 `txcaptcha.apk`。

我使用了 BlueStacks 安卓模拟器安装该APK。

### 3. 滑动验证码

滑动验证码有以下三种验证方式：

* 方式一

配合MCL命令行，在APK中输入请求码地址

注意：新注册的账号会出现如下报错

```cmd
[CIRCULAR REFERENCE:net.mamoe.mirai.network.WrongPasswordException: Error(bot=Bot(2088667670), code=237, title= 禁止登录, message=当前上网环境异常，请更换网络环境或在常用设备上登录或稍后再试。, errorInfo=), tips=若频繁出现, 请尝试开启设备锁]
```

但如果我使用我自己的老QQ号，就可以正常登录。

***注意：新账号需要登陆几天(挂机)后再使用***

* 方式二：

在命令行中，会得到华东验证码的URL地址，如`https://ssl.captcha.qq.com/template/wireless_mqq_captcha.html?style=xxx...xxx` 此时，将URL前缀 `ssl.captcha.qq.com` 换成 `txhelper.glitch.me`，将其填写到浏览器地址栏。

此时根据浏览器提示，在手机APP中输入验证码的请求码，得到滑动验证码。

完成滑动验证后，再次在浏览器中刷新页面，得到tickets填入框中。

* 方式三：

安装 miraiandroid 软件，实现本地登录

可参考： https://install.appcenter.ms/users/mzdluo123/apps/miraiandroid/distribution_groups/release

</details>

---

## 二、插件说明

目前测试QQ号已添加的插件如下：

### 1. 随机色图插件(suijisetu)
* https://github.com/Ycituss/suijisetu
* https://gitee.com/ycycycc123/suijisetu
* 配置位置： `Development/config/Setu/ApplicationConfig.json`

### 2. 图灵机器人

* https://github.com/Nambers/Mirai-TuLingBot
* https://mirai.mamoe.net/topic/86/mirai%E6%8E%A5%E5%85%A5%E5%9B%BE%E7%81%B5%E6%9C%BA%E5%99%A8%E4%BA%BA
* http://www.tuling123.com/member/robot/2364676/center/frame.jhtml?page=0&child=0
* 图灵APIKEY: 6dd2c05f0865424db768c6609b3c57c6
* 配置位置： `Development/data/TuLingBot/config.json`

## 三、linux环境搭建

与 Windows 一样，使用mcl启动器：https://github.com/iTXTech/mcl-installer/releases

若使本项目在Linux环境运行，只需执行 `Development/mcl` 文件即可。

具体配置请参照插件说明章节。

## 四、项目地址

* Mirai-Linux : [https://github.com/ZHJ0125/Mirai-Linux](https://github.com/ZHJ0125/Mirai-Linux)
* Mirai-Windows : [https://github.com/ZHJ0125/Mirai-Windows](https://github.com/ZHJ0125/Mirai-Windows)


