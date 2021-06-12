---
layout: post
current: post
thumbnail:
navigation: True
title: JetBrains Night Seoul 2017
date: 2017-11-21
tags: [etc]
class: post-template
subclass: 'post tag-etc'
author: raw-coder
published: false
---

## JetBrains Night Seoul 2017 후기

IntelliJ 라는 좋은 IDE를 개발한 JetBrains에서 개최하는 JetBrains Night Seoul 2017(서울 양재 엘타워, 2017-11-19)에 다녀왔습니다.

저는 최근 1년간 IntlliJ IDEA 기반의 Android Studio, WebStorm 을 IDE로 사용해오고 있었기에 이전부터 관심있는 행사였고, 운좋게 참석할 수 있었습니다.

컨퍼런스 장소인 양재역은 회사에서 퇴근하는 길이라 평일 저녁시간에 개최되었지만 부담없이 참석할 수 있었습니다.

첫번째 세션이 열리고 30분 정도 후에 컨퍼런스 장소에 도착하였는데, 500여명이 넘는 참석자들의 열기에 놀랄 수 밖에 없었습니다.

첫번째 세션은 하디 하리리가 직접 코딩을 하면서 intelliJ의 좋은 기능을 소개하는 시간이었습니다.

Tips and trick 이라는 제목의 세션이었는데, 자세한 내용은 인터넷으로 찾아보는 것이 나을것 같고,
VP 라는 높은 직책의 중년 개발자가 수백명 앞에서 라이브 코딩을 하며서 그들의 제품에 대한 소개를 열정적으로하는 모습은 굉장히 인상적이었습니다.

다음 세션은 JetBrains사의 각종 협업 툴에 대해 소개하는 세션이었습니다. 이슈 트래커인 Hub, CI/CD 툴인 Teamcity, 코드 리뷰 툴인 Upsource의 주요 기능들에 대해 소개하고 시연하는 모습을 볼 수 있었습니다.
평소 사용하는 Jira, Trello, Bitbucket 과 유사한 기능이었지만, 좋은 IDE를 만드는 회사에 대한 신뢰감이 바탕이 되어 좋은 제품이라는 인식을 가지게 되었습니다. 유려한 UI는 한번쯤 사용하면 좋겠다는 생각이들 정도였습니다.

### Tips and trick
JVM debugger
functional p debugging
sql query support
Rest client view
Metrics Reloaded Plugin
code folding plugins

### Continuous Workflow
Hub : issue tracker
Teamcity : CI/CD tool
  remote
Upsource : code review tool

### Kotlin 102 - beyond the basics
lateinit
: Datatype by somefunction()
higherOrderFunction
extensionFunction
  infix annotation
  "hello".isTheSameAs("Helllo")
  "hello" isTheSameAs "Hello"
inline function
  inline fun <refied T> someFunction(input: List<Any>)
typealias
  typealias CustomerName = String
lazy evaludation
  numvers.filter{it < 90}.sortedBy{ it}
  number.asSequence().filter .... => lazy eval.
invoke
  operator fun invoke(function: HttpResponse.() -> Unit)
sealed
  sealed class Result
  open class Result
coroutine() vs thread()

### 레진코믹스는 Kotlin을 어떻게 사용하고 있을까? - 우명인 님
왜 사용하고 있을까? 이전 발표 있었음...
why Kotlin?
  Java와 호환
  lambda, higher-order function
  boiler plate 적음
  null safe, kotlin extension, ...
why Java?
  익숙함, 성능?
k vs j code = 54: 45
pros
  java 100%
  lambda expression
  validationCheck : require, check
  higher-order function
  kotlin extension
  android extension
  lateinit :runtime에 할당되는 mutable property, by lazy : runtime에 할당되는 readonly property
  collection API
  FP
cons
  kapt
java -> kotlin
  2-3months needed
  data -> ui -> biz code  
