# Tik-Tok-
Tik Tok
# 前情提要：
下载链接 ：IOS旧版应用 https://app.even.stream
这个网站可以下载到文中需要的App

# 教程分2大步骤
 【1】：先部署环境【安装证书+添加规则】
 【2】：下载旧版TikTok 21.1.0版本以下(包含21.1.0)

# 以下为详情操作步骤：

# 【1】部署环境部分

  安装最新版Shadowrocket，【美区AppStore下载，或用上面的链接】

  生成证书文件（步骤如下）
1. 打开App 点击配置 – 在[本地文件]点击一个配置文件（默认是default.conf）- 选择旁边的 i – 编辑配置 – HTTPS 解密 – 打开HTTPS 解密开关 – 生成新的 CA证书 – 生成新的 CA证书 –  安装证书 如果在这个步骤卡在“强制安装证书”页面，点击“强制安装”也无效的情况下，点右下角Safari浏览器图标，使用Safari打开就可以正常安装了

2.点右上角 – 安装 – 按要求输入手机锁屏密码 – 再次点右上角 – 安装 – 安装 – 右上角 – 完成

3.打开手机 – 设置 – 通用 – 关于本机 – 证书信任设置 – 找到 – Shadowrocket开头的选项 – 打开右侧开关 – 弹出警告框 – 继续

4.再次打开Shadowrocket App – 配置 – 找到[本地文件]内的配置文件，默认是[default.conf] – 点击 – default.conf – 编辑纯文本

翻到[URL Rewrite]位置[大概在568行]，在它下面一行粘贴以下代码:

(?<=_region=)CN(?=&) US 307

(?<=&mcc_mnc=)4 2 307

^(https?:\/\/(tnc|dm)[\w-]+\.\w+\.com\/.+)(\?)(.+) $1$3 302

(^https?:\/\/*\.\w{4}okv.com\/.+&.+)(\d{2}\.3\.\d)(.+) $118.0$3 302 
 

5.然后再找到[MITM]，再它下面粘贴以下代码

 hostname = *.tiktokv.com,*.byteoversea.com,*.tik-tokapi.com  

6.然后点击右上角 – 保存


7.最后返回首页添加节点【如有问题则提问如何获得和添加节点】；

8.然后全局路由选择配置，然后开启连接（首次开启需要验证 – Allow – 指纹/密码）

9.开启TikTok【已经成功安装旧版】


# 【2】安装旧版TikTok
1.有能力的自行谷歌抓包旧版下载，这里不展开了。

2.登陆别人Apple ID 下载已经抓好的旧版TikTok。此为链接: IOS旧版应用 https://app.even.stream
，网页上有操作详情步骤：
【注：二次验证的验证码，请选择发短信，不要发送给设备。不是我的设备，我只是搬运工。】

# 到此结束

文中提到的代码如下，可以直接复制
----------------------------------------------------------------------------------------
[URL Rewrite]
(?<=_region=)CN(?=&) US 307
(?<=&mcc_mnc=)4 2 307
^(https?:\/\/dm[\w-]+\.\w+\.com\/.+)(\?)(.+) $1$3 302
(^https?:\/\/*\.\w{4}okv.com\/.+&.+)(\d{2}\.3\.\d)(.+) $118.0$3 302

[MITM]
hostname = *.tiktokv.com,*.byteoversea.com,*.tik-tokapi.com
----------------------------------------------------------------------------------------

-*snssdk.com, -*amemv.com
【以上，感谢电报群里的大佬们！整理者电报频道：https://t.me/huangdi321】

另附赠 安卓TikTok链接【 破解版apk文件】
TikTok1.2.2 apk https://drive.google.com/file/d/1Vo4wLDvKgWGQkv_iVBSW4drbSg5HE25W/view?usp=sharing
