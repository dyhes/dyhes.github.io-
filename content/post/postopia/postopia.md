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

## Hard Core

### Spring Security

没有经验时的登录实现，文档杂乱，不知道如何寻找正确的实现方法

## Inspiration

### w5

如何处理以前没有遇到过的新需求（如给用户发送邮件），需要积累解决问题的能力（实习的时候可以边问边查，做自己的项目只能自己去查，那么如何高效检索并善用AI）,并形成方法论，以便提高能力


## Best Practices
很多问题只有亲身经历才能体会，并寻求 best practices 比如:
* 直接更新好，处理可能的异常好还是先查询存在再更新好
* 是否在Service Layer 使用@AuthenticatedPrincipal
* service引用多个repository或引用对应repository和其他service

## Performance Considerations
* 用户对于帖子或评论的态度（赞同，反对）是否用额外的query查询更好（w4）