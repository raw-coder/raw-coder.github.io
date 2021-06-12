---
layout: post
current: post
thumbnail: assets/img/javascript.png
navigation: True
title: JavaScript 비동기 처리 정리
date: 2018-1-3
tags: [javascript]
class: post-template
subclass: 'post tag-javascript'
author: raw-coder
published: true
---

## javascript 비동기 흐름제어 정리

promise, generator function, async - await 를 이용한 비동기 처리 방법을 정리합니다.

> callback function 을 이용한 비동기처리

``` javascript
const fs = require('fs')

fs.readFile('a.txt', 'utf-8', (err, data) => {
  console.log(data)
  fs.readFile('b.txt', 'utf-8', (err, data) => {
    console.log(data)
    fs.readFile('c.txt', 'utf-8', (err, data) => {
      console.log(data)
    })
  })
})
```

> promise 를 이용한 비동기처리

``` javascript
const fs = require('fs')

function readFilePromise(fileName) {
  return new Promise((resolve) => {
    fs.readFile(fileName, 'utf-8', (err, s) => {
      resolve(s)
    })
  })
}

readFilePromise('a.txt')
.then((text) => {
  console.log('reading a.txt has finished\n', text)
  return readFilePromise('b.txt')
})
.then((text) => {
  console.log('reading b.txt has finished\n', text)
  return readFilePromise('c.txt')
})
.then((text) => {
  console.log('reading c.txt has finished\n', text)
})
```


> generator function 을 이용한 비동기 처리

``` javascript
const fs = require('fs')

function readFileGenerator(g, fileName) {
  fs.readFile(fileName, 'utf-8', (err, data) => {
    g.next(data);
  })
}

const g = (function * () {
  const a = yield readFileGenerator(g, 'a.txt')
  console.log(a)
  const b = yield readFileGenerator(g, 'b.txt')
  console.log(b)
  const c = yield readFileGenerator(g, 'c.txt')
  console.log(c)
})()

g.next()
```

> async - await 를 이용한 비동기 처리

``` javascript
const fs = require('fs')

function readFilePromise(fileName) {
  return new Promise((resolve, reject) => {
    fs.readFile(fileName, 'utf-8', (err, data) => {
      resolve(data)
    })
  })
}

async function readAll() {
  const a = await readFilePromise('a.txt')
  console.log(a)
  const b = await readFilePromise('b.txt')
  console.log(b)
  const c = await readFilePromise('c.txt')
  console.log(c)
}

readAll()
```
