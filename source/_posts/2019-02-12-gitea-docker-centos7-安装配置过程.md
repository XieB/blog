---
title: gitea docker(centos7)安装配置过程
date: 2019-02-12 10:54:02
tags:
---

##### 安装docker,参考官方教程（建议使用最新版本）
`curl -fsSL https://get.docker.com/ | sh`
&nbsp;
##### 添加开机启动
`systemctl enable docker`
&nbsp;
##### 拉取gitea docker镜像
`docker pull gitea/gitea:latest`
&nbsp;
##### 创建挂载目录,保证重启docker数据不丢失
`sudo mkdir -p /var/lib/gitea`
&nbsp;
##### 创建docker容器
`docker run -d --name=gitea -p 10022:22 -p 10080:3000 -v /var/lib/gitea:/data gitea/gitea:latest`
> 创建一个name是gitea,容器端口22映射到母机10022、3000映射到母机10080，挂载母机/var/lib/gitea到docker容器内作为/data挂载点

> 登入后会让你填写基本信息，数据库建议选择sqlite，免去安装数据库的麻烦。

&nbsp;

##### 配置文件
> 安装完成后，修改配置文件conf/app.ini

```
SSH_PORT         = 20022 //web页面显示的ssh端口
LANDING_PAGE = explore //默认显示登录页
```