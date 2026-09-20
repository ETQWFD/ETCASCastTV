# ETCAS投屏客户端（ETCAS Cast TV）

ETCAS投屏 的 Android TV 接收端。手机端通过同一局域网内的 DLNA/UPnP 协议发现并连接本客户端，把本地视频、图片、网页视频或手机屏幕镜像投到电视上。

- 包名：`com.etc.cas.tv`
- 最低系统：Android 7.0（API 24），支持 32 位 / 64 位 / x86 设备
- 开源许可：MIT

## 主要功能

- 开机自启，前台服务常驻，启动后自动可被手机发现
- 标准 DLNA/UPnP MediaRenderer，兼容哔哩哔哩云视听小电视、酷喵、芒果 TV、奇异果等同类投屏
- ETCAS 私有配对：手机端扫码或手动添加本设备时，需输入电视屏幕上显示的配对码
- 接收本地媒体、网页链接投屏，以及手机屏幕镜像（低延迟逐帧画面）
- 每次启动自动检查更新，发现新版本可选择在应用内下载并安装，安装后自动清理安装包

## 连接方式

1. 电视与手机连接同一个 Wi-Fi
2. 打开本客户端，主界面会显示连接 IP、配对码与二维码
3. 手机端 ETCAS投屏 点击投屏搜索本设备，或直接扫码，按提示输入配对码
4. 在手机上选择视频 / 图片 / 网页 / 屏幕镜像并开始投屏

## 编译

使用 Android Studio 打开本目录，或：

```bash
gradle :app:assembleRelease
```

发布签名使用 `keystore/etcas-tv.jks`（口令见 `gradle.properties`），可用自己的签名替换。

## 许可

MIT License。致敬开发者：ETC协会；翻译：POAI。官网：https://etc.os.kg
