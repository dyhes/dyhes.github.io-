---
title: 【Postopia Dev Log】Summary
date: 2024-07-05 00:00:00+0000
image: /covers/cover18.png
categories: 
    - moon
    - snow
tags:
    - Postopia
math: true
---
考虑性能

考虑隔离级别

很多问题只有亲身经历才能体会，并寻求 best practices 比如:
* 直接更新好，处理可能的异常好还是先查询存在再更新好
* 是否在Service Layer 使用@AuthenticatedPrincipal