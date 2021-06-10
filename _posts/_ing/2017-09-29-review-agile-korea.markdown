---
layout: post
title: "Agile Korea 2017을 다녀와서"
date: 2019-09-29
categories:
  - Review
description: Agile Korea 2017 후기
image: assets/img/agile-korea-2017.png
image-sm:assets/img/agile-korea-2017.png
---

어느덧 Agile 개발 문화를 통한 변화를 주도하는 팀에 합류한지 1년여가 흘렀다.
팀에 합류한 이후 Agile 방식으로 일하면서 그동안 몇가지 프로젝트를 수행하였다.
어느 프로젝트에서는 Agile에 대한 열렬한 광신도가 되어 눈이 벌게지도록 개발을 하기도 하였고,
어떤 프로젝트에서는 여러가지 장애물에 부딪혀 좌절하고 이대로 괜찮은가를 항상 되뇌이며 고뇌의 나날을 보내기도 하였다.

때마침 5년만에 열리는 국내 Agile 최대 모임 Agile Korea 2017에 다녀왔다.
존경하는 팀리더 휴벗님은 우리 회사뿐 아니라 국내 Agile 개발 문화 자체를 주도하는 개척자(pioneer)이다.
그분을 중심으로 내로라하는 분들이 모여 오랜 준비끝에 행사가 개최되었다.

부끄럽지만 나는 Agile 초보자 입장에서 구경하는 기분으로 참석만 하였다.  매일 출근하는 곳에서 개최되었고 주변에서 늘상 접하는 주제들이 여기저기서 들려오긴 했지만, 정말 많은 분들이 관심을 가지고 참석해주셨다. 색다른 기분이었다.

이번 Agile Korea 2017은 '리빌딩 애자일 커뮤니티'라는 모토로 개최되었다.

### Keynote : The State of the Art in Agile - Mike Mason (CTO, Thoughtworks)

Agile has won! 94% 도입하고 있음
98% 성공하고 있음을 체감
여전히 갈길은 멀다 80%은 멀었ㄷ라고 응담

지난 16년간 Agile 을 통해 무었을 성취했나
Thoughtworks : Think Big, start samll go fast

Mingo : 애자일 관리 툴
경험은 80 books로...

individual Dev 입장에서
스크럼
TDD : Red -> Green -> Refactoring : 지속적인
테스트 pyramid :  unit - service - integratin - UI
Command Line Builds and fequent commits : 10분이내 빌드완료, 여러번 나눠서 커밋

An Agile Team
Pair Programming : fundamental of agile Programming
higher quality , knoleadge sharing
Continuous Integration :

Trunk-based Development :모든 사람이 변화를 공유하는 것..
반만 완성된 코드 : Feature Togle 을 통해... on 한 유저만 사용..
Continuous Delivery

Teams in an Organization
Agile software architecture
==> Architecture 은 Testability에 매우 중요
light weight, less coupled

- sprify 사례 : cross-opllination > standadization

6~10 people Team : communtioncation 비용측면에서 적절한 팀 규모
팀간은 API, CDs 로 연결

Consumer-driven Contacts
: Contract Validator 로 Billing, Order, Marketinng service 묶어줌.. 사례

Micro Services
monolithic appliation vs micro service application

Conway's Law
Architecture 는 조직이 커뮤니케이션하는 방식을 그대로 반영한다

ex) API Team, Business Logic Team Data Team => MS1(API + Buisiness Loginc + Data) + MS2 ...

DevOps : 71% 이미 하고 있거나 계획중임

**Enterprise Build and Deploy (출처 puppet.com)
퍼포먼스가 높은 조직은 개발자가 많아질수록 Deploy 빈도가 매우 높아짐!!!
반대는 점점 낮아짐!!**

You build it, you Run it : Amazon

Very Large Organization
- Platform
- API Ecosystems : 내부 API ...

Product!! not Project!
제품 중심의 생각.. 좀 더 장기적인 관점에서

Hypothesis-Driven Development?

Netflix :  당신들도 좋은 사람들을 가지고 있었다...

Q 위계질서 강한 한국 조직사회에서 어떻게...
작게 조직을 나눈다. spotify 가 좋은 사례...

Q 스프린트 중간에 끼어드는 이슈는 먼저처리하는 것이 맞는지 막고 다음 스프린트에서 처리하는 것이 맞는지..
팀의 상황에 따라 다르다.

Q 이상적인 상황이 아닌 좋은 개발자와 엔지니어가 부족.. 일반적으로 여러개의 프로젝트를 수행하게 된다. 어떻게 시간을 나누어 효율적으로 프로젝트를 수행할 수 있나...
IT에서 테크 리드의 가장 중요한 역할은 코딩이 아니라 팀을 키우는 일이다! 그것에 중점...

### 애자일 전파를 위한 혼자만의 싸움 전략 - SK 플래닛, 신원 ###
15년차 개발자. 2년 애자일 코치

일반적으로 일보다 사람을 통해 받는 스트레스가 크다.
애자일은 사람간의 문제를 해결하기위한 철학, 여러가지 방법들의 집합이다.

발표주제는애자일을 시작하려는 사람들을 위한 이야기..

SK 플래닛은 애자일 도입 9개월..
방항에 대응 : 조직구조개편, 애자일교육, 애자일 경험 직원 채용,

이해도, 감정/태도 측면에서 다양한 사람들이 존재

크로스 펑셔널팀을 구성하는데 적용 어려움.. Deb, UX, PM 별 팀(pool)이 따로 있음

Agile Manifesto
왼쪽도 중요하지만 오른쪽이 더 중요하다.
그러나 각자 편한대로 생각한다.

* 싸움기술
- 마음을 편히 갖자
애자일 책으로만 배우면 좋은 점과 성공에 대해서만 생각에 남는다. 하지만 현실은 아니다.
100% 성공하기는 어려움.. 지속적인 개선이란 명목하에 추후개선한다고 생각
회사의 문화를 만드는 것이 가장 어려움 그것에 중점

- 전우를 모으자
혁신 수용 곡선(에버렛 로저스 혁신의 확산이론)에서 혁신자 2.5%, 초기수용자 13.5%을 모으기 위해 사내 커뮤니티 활성화
불특정다수의 저항하려는 사람보다 변화를 열망하고 받아들이려는 사람에게 집중

- 퍼트리자
교육도 페르소나에 맞는 수준별 강의 커리큘럼 구성하자
(Beginner : 흥미만 느끼게 하자, Intermediate: 실무 적용에 대한 의지, Advanced:학습 연습 피드백 전파 준비)
멘토링 코칭

- 여유를 만들어주자
업무 시간의 대부분은 회의 => 줄일 수 없다면 효율적으로 ..
퍼실리테이션 : 업무 진행을 위해 가장 중요. 퍼실리테이션 스킬을 먼저 배우면 Good!

- 유능한 애자일코치가 더 필요
내부 애자일 코치가 핵심!
애자일 코칭은 장기간의 수행, 훈련이 필요
아무나 할 수 있을지도 모르나 잘하기는 어렵다.. 퍼실리테이션만 제대로 하는데 5년 훈련 필요?
Agile Coaching Framework

Q 애자일 조직을 평가하기 위한 KPI 정량적 지표 (보고용) 은 어떤것을 사용하지??
평가하기 여려움..
애자일 문화에 대한 서베이 점수
리드타임?? 보고용으로 는 매우 어려움..

Q 스몰 마우스 격려 방안 ?
글로 써서 아이디어 나누는 등의 기법..

Q 퍼실리테이션?
사람들이 의견 도출, 의견 조율하는 기법

### keynote : Design for growth, A tatcical toolkit for middle management : the leader of knowledge workders - Luk Lau (Enterprise Agile Coach, Twitter) ###

Organizational Design for growth for management
no fluff, Just Stuff
By movement, not mandate

- 전구는 양초가 CI되어 만들어지지 않음 - Oren Hariari

#### Today outcome
Why  the urgency to actuallywhy necesith to Designhow to design sustainable changes

####
Ways to deal with a problem - reaktor..
dissoultion
soultion
resoution
absolution



#### Optimization ===> Adaptation
#### Nature of Workers : Manuel worker, knowledge workder, learing Worker
#### Go Agile !!!  : management 빠져있었음...

Lead Diffently
Agile leadershi journey
expert , achiever => catalyst, co-creator, synergist

- leadership by tail ridge

##### Diminishers vs multipliers

#### Why design matter
without chaniging our patterns of thought, .... 아인슈타인 - AZ Qutes
To manage a system effectiveyl, you might focus on .... Russel ackoff...

#### Design thinking ...
Design Sprint - by Google
Brainstoriming ==> Gamestorming / Innocation Gamestorming

How to start a movement  - youtube

change key :
urgnecy!
how to

### 소 잡는 칼(마이크로 서비스), Riot Games 지두현
Architecture : Monolithic ===> Micro services

MSA 가 CI/CD 측면에서 이점이 있음. 개발자 선호

LOL Account Security (계정 봔)사례
if-else 복잡도 ==> message bus 구현하여 해결..

Kafka - distributed streaming platform
각 단계에 publisher 와 consumer를 MSA로 구현

--> kibana dashboard 활용

MSA에서 Centalized logging and monitoring 은 필수!

backend, frontend Microservice 를 구분하여 개발

mocking site를 통해 작업..
swagger json payload 확인 적극 활용

모든 서비스는 sharing되는 storage를 갖지 않는다. 자기 자신에게만 종속되게 한다..


#### 라이엇 게임이 애자일을 했는지??
프랙티스를 준수하는 것에 목표를 두지 않음..

microservice당 티밍 단위는 보통 2명, 1~3명

planning, retro는 별로 필요없었음

그러나 애자일을 수행했다..

스프린트에서 달성해야할 목표와 그 목표를 방해받지 않고 달성하는 방법에만 집중했다.

engineering.riotgames

애자일 조직에서의 소프트웨어 아키텍트 - NBT 남상균

애자일, 한때의 유행인가 - 조승빈
