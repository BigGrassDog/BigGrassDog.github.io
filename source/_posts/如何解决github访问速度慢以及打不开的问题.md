---
title: 如何解决github访问速度慢以及打不开的问题
date: 2021-09-02 10:49:52
tags: github
---

# 查询 <font color=Red>github</font> ip 地址

[网址查询](https://github.com.ipaddress.com/)
[域名查询](https://fastly.net.ipaddress.com/github.global.ssl.fastly.net)
[静态资源 ip](https://github.com.ipaddress.com/assets-cdn.github.com)

# 修改 host 文件

```
140.82.113.4  github.com
199.232.69.194  github.global.ssl.fastly.net
185.199.108.153  assets-cdn.github.com
185.199.109.153  assets-cdn.github.com
185.199.110.153  assets-cdn.github.com
185.199.111.153  assets-cdn.github.com
```

<!--more-->

# 刷新 DNS 缓存

```
ipconfig /flushdns
```
