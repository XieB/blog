---
title: android系统升级webview方法
date: 2020-04-17 21:16:52
tags:
---
- 使用adb connect 192.168.1.135连接安卓设备，如果提示
`cannot connect to 192.168.1.135:5555: 由于目标计算机积极拒绝，无法连接。 (10061)`
- 下载adbwireless.apk安装到android设备上，重新尝试
- 使用如下命令
`adb shell`
- 进入android命令行，找到webview的目录
`/system/app/webview`
- 执行备份操作
```
mount -o rw,remount /system // 重新挂载,否则无法写入
cd /system/app
mv webview webview-b
mkdir -p webview/lib/arm
```
- 下载好的.apk 直接改成 .zip 然后解压缩，复制出libwebviewchromium.so,同webview.apk一并覆盖
```
/system/app/webview/lib/arm/libwebviewchromium.so
/system/app/webview/webview.apk
```
- 设置执行权限
`chmod 777 webview/*`
- 重启
`adb reboot`
- 失败了,先用安卓包内置webview解决吧