---
layout: post
current: post
thumbnail: assets/img/javascript.png
navigation: True
title: 번역 - Resilient Distributed Datasets A Fault-Tolerant Abstraction for In-Memory Cluster Computing
date: 2018-1-10
tags: [translation]
class: post-template
subclass: 'post tag-translation'
author: raw-coder
published: false
---

## [번역] Resilient Distributed Datasets: A Fault-Tolerant Abstraction for In-Memory Cluster Computing

RDD 를 세상에 소개한 논문 Resilient Distributed Datasets: A Fault-Tolerant Abstraction for In-Memory Cluster Computing 을 번역합니다.

[논문링크](https://www.usenix.org/system/files/conference/nsdi12/nsdi12-final138.pdf)


### Resilient Distributed Datasets(RDDs) : 인메모리 클러스터 컴퓨팅에서 장애 허용을 위한 개념

#### 요약
We present Resilient Distributed Datasets (RDDs), a distributed
memory abstraction that lets programmers perform
in-memory computations on large clusters in a
fault-tolerant manner
장애 허용 분산 메모리 개념인 Resilient Distributed Datasets(RDDs)을 소개한다.

RDDs are motivated by two types
of applications that current computing frameworks handle
inefficiently: iterative algorithms and interactive data
mining tools.
RDD는 반복적인 알고리즘에 의한 비효율적인 최근의 연산 프레임워크와 인터렉티브한 데이터 마이닝 툴과 관련된 어플리케이션의 영향을 받았다.

In both cases, keeping data in memory
can improve performance by an order of magnitude.
두가지 경우 모두에서, 데이터를 메모리에서 가지고 있는것은 퍼포먼스를 대량으로 향상시켰다.

To achieve fault tolerance efficiently, RDDs provide a
restricted form of shared memory, based on coarse-grained
transformations rather than fine-grained updates
to shared state.
장애 허용성을 효율적으로 달성하기 위하여, RDD는 상태에 대한 공유를 위해 상세한 갱신보다 대략적인 변동?에 기반한 공유 메모리에 대한 제한된 양식을 제공한다.  

However, we show that RDDs are expressive
enough to capture a wide class of computations, including
recent specialized programming models for iterative
jobs, such as Pregel, and new applications that these
models do not capture.


We have implemented RDDs in a
system called Spark, which we evaluate through a variety
of user applications and benchmarks.
