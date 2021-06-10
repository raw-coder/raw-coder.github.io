---
layout: post
current: post
thumbnail: assets/img/javascript.png
navigation: True
title: Generator 를 활용한 피노나치 수열 예제
date: 2018-1-3
tags: [javascript]
class: post-template
subclass: 'post tag-javascript'
author: raw-coder
published: true
---

## ES6에 추가된 Generator 함수에 대해 간단히 정리합니다

* **function \*** 키워드로 정의
* **yield** 구문을 반드시 포함하여햐 함
  * return 구문과 유사하게 값을 반환
  * return 구문과 다른 점은 return은 한번만 값을 반환하지만, yield 구문은 여러번 실행됨

``` javascript
// gernerator 함수 counter 정의
function * counter() {
  yield 1
  yield 2
  yield 3
}

const g = counter()
console.log(g.next())
console.log(g.next())
console.log(g.next())
console.log(g.next())
```

``` terminal
{ value: 1, done: false }
{ value: 2, done: false }
{ value: 3, done: false }
{ value: undefined, done: true }
```

아래 예제는 gernerator를 활용한 피보나치 함수 구현 예제 코드 입니다

``` javascript
function * getFibonacci() {
  let a = 0
  let b = 1
  while (true) {
    [a, b] = [b, a + b]
    yield a
  }
}

const fib = getFibonacci()
for(const num of fib) {
  if (num > 50) break
  console.log(num)
}
```
