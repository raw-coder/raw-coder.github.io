---
layout: post
current: post
thumbnail: assets/img/javascript.png
navigation: True
title:
date: 2018-1-12
tags: [translation]
class: post-template
subclass: 'post tag-translation'
author: raw-coder
published: false
---

<!--  TODO : 정리 !!!! -->
SpringOne Platform Recap


## 정윤성 님 - SpringOne Keynote Recap

Nokia 폰 사례 ==>  변화.. 스프링은 같은 시대에 출시되었으나 여전히 많이 사용

update vs 가용율 그래프

Caitie McCafrey
-> optimize for making your code easy to modify

변화에 대한 대응이 핵심!

소프트웨어 메인터넌스는 현재의 상태에 대한 버그 픽스보다.. 이전보다 개선하는 데 초점을 두여야함

Spring Initializer 로 시작하라

Spring In.. 통계
View : Thymeleaf >>> FreeMarker, Mustache, Groovy Templates 순
NoSQL: JPA >>> MongoDB, Redis, Elastic, Cassandra ...

12 Factor Apps..
===> Cloud Native applications + Serverless

Springboot + Spring cloud on Pivotal Cloud foundary ==> good


### Spring new Features
* Kotlin 지원  ---> Groovy 압도...
* Reactive 지원 : Event-Driven 구현
  -- WebFlux - Data, Boot, Security 기본  Runtime 도구 tomcat 대신 netty 선택..
  * Servelet(Blocking IO 모델 -- Spring MVC), Reactive Stack 선택 가능.. ( Swimming Pool Lane vs AirPort 예)


중요 update
* Synchrounous Blocking I/O ==> Non Blocking I/O 지원
  * Reactor 를 통해 양쪽 사용 가능하도록 지원
  * live coding demo 꼭 보기!!

* springboot 2.0
* Spring Tool 4 : not XML
* IBM 협업..
* Pivotal Cloud Foundary ==> pivotal container service
  cf_push
  * .Net 지원 강화

## 노경훈 님 -  성공사례 with Pivoal pivotal Korea 대표

Pivotal Service 왜 쓰나??
### Boeing 사례 -  Speed
문화변화 너무 어려움 --> DTE, platform을 먼저 바꾸면 잘되었음

### Scalabity - T-mobile
8명으로 11000개 컨테이너 관리 도입 1년만에!! -- 영상 참조

### 미공군 사례
공중 급유 Tanker Planning 개발...
===> 문화가 중요하다..


The only thing constant in life is CHANGE - Heraclitus

Learn
미래 예측 무의미.. 조직이 빨리 변화에 대응할 수 있도록 하는 것이 중요


## PCF, PKS - 신혜원님 pivotal 아키
클라우드 네이티브 앱을 개발하기위한 플랫폼

### PAS pivotal application Service
Spring Boot로 간편하게 생성한 jar로 컨테이너 생성하여
개발, 배포환경에서 서비스 -- cf_push

kubernetes : 컨테이너 관리!!!

### PFS - serverless



## Serverless Spring : 오충현 님 solution Architect

### serverless ?
Backend as a Service: BaaS
Function as a Service: FasS**
둘 혼용하여 사용
-firebase, 람다, google azure function
===> 서버는 존재하지만 관리하지는 않음..

### why serverless?
cost reduction
productivity
efficient operation
resource resusabillity

openWhisk.. opensource

### ICE 법칙 : 3가지중 2가지만 선택가능
Immediate :Instance on
Consistent : Immutable containers
Effiient Scale to Zero
요청발생시 함수 컨테이너 실행 최초 실행 느림
실행 중인 컨테이너에 함수 코드 주입 컨테이너 환경의 일관성 저해
함수 컨테이너를 계속 실행 리소스 점유

### Riff 프로젝트

java function 올리는 시연
string to upper case
string stream(Flux) to lower case

### 시연
Enterprise Paas Heroku, App Engine =====> Spring Cloud Foundary
Enterprise Fass function, lamda ===> riff


## Spring Framework, Reactive programming

Netflix 사례 : 테크 블로그
MSA, rxJava

### Spring framework 5.0 overview
* Reactive Stack
* Servlet Stack

### 기억할 내용
Back-Pressure : Reactive 데이터 흐름 제어
Reactive Spring Data ~ repository
Function Reactive programming
Project Reactor

### Reactive


### Java Stream vs Flux / Mono
pull base | push based
No flow control | Back-pressure strategy

==> MongoDB
List, Class 리턴 ==> Flux, Mono 리턴으로 구현 Reactive mongo operation

### 시연
-mongoDB 조회

-github.com/myminseok/s1p-reactor-in-???
테스트
