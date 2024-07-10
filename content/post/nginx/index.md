---
title: 【NGINX】浅尝
# description: Math typesetting using KaTeX
date: 2022-11-09 00:00:00+0000
categories: 
    - nutrition
tags:
    - nginx
math: true
---


## Introduction

Nginx is a web server that can also be used as a reverse proxy, load balancer, mail proxy and HTTP cache.

> Nginx是可以用于反向代理，负载均衡，邮件代理和HTTP缓存的Web服务器

![](https://img2022.cnblogs.com/blog/2369386/202211/2369386-20221109201921081-1294800408.png)


## Installation

ubuntu:

```bash
sudo apt install nginx
```

**查看状态**

```bash
systemctl status nginx
```

![](https://img2022.cnblogs.com/blog/2369386/202211/2369386-20221109202023436-1812887101.png)


**管理**

```bash
sudo systemctl stop nginx

sudo systemctl start nginx

sudo systemctl restart nginx

sudo systemctl reload nginx  ##configuration changed
sudo nginx -s reload

sudo systemctl disable nginx ##disable the behavior of starting automatically when the server boots

sudo systemctl enable nginx
```

## Terminology

* context

  ```nginx
  events {
  	...
  }
  ```

* directive

  ```nginx
  worker_connections 768;
  ```

  context内的键值对

## Load Balance

![](https://img2022.cnblogs.com/blog/2369386/202211/2369386-20221109202105232-1499985114.png)
![](https://img2022.cnblogs.com/blog/2369386/202211/2369386-20221109202120702-1771113407.png)

## Bugs

### css text/plain

NGINX: CSS was not loaded because its MIME type, "text/plain", is not "text/css"

修改为

![](https://img2022.cnblogs.com/blog/2369386/202211/2369386-20221109202136034-795829651.png)


后仍未加载

原因为**浏览器缓存**

`Ctrl+Shift+R` hard reload 解决问题