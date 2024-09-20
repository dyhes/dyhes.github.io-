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
考虑隔离级别

## best practices
很多问题只有亲身经历才能体会，并寻求 best practices 比如:
* 直接更新好，处理可能的异常好还是先查询存在再更新好
* 是否在Service Layer 使用@AuthenticatedPrincipal
* service引用多个repository或引用对应repository和其他service

## Performance Considerations
* 用户对于帖子或评论的态度（赞同，反对）是否用额外的query查询更好（w4）