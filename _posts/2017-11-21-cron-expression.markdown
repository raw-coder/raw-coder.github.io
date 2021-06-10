---
layout: post
current: post
thumbnail: assets/img/cron.png
navigation: True
title: Cron 표현식
date: 2017-11-21
tags: [etc]
class: post-template
subclass: 'post tag-etc'
author: raw-coder
published: true
---

## Cron 표현식
Batch Job 개발에 필요했던 Cron 표현식 간단히 정리합니다.

``` terminal
* * * * *       # 분(0-59) 시(0-23) 일(1-31) 월(1-12) 요일(0-6)
30 6 * * *      # 매일 6시 30분
*/10 * * * *    # 매 10분 마다
```
