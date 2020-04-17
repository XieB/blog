---
title: vue项目history模式tomcat配置
date: 2020-04-17 19:30:29
tags:
---
- 在网站根目录新增文件WEB-INF/web.xml,内容如下
```
<web-app>
<error-page>  
<error-code>404</error-code>  
<location>/index.html</location>  
</error-page>  
</web-app>
```
- 需要重启tomcat