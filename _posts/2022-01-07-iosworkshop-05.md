---
title: "[Swift 문법 정리] 연산자(Operator)"
date: 2022-01-07
categories:
  - Swift
tags:
  - swift
  - operator
  - 연산자
toc: true
toc_label: "목차"
toc_icon: bars
toc_sticky: true
---

### 기본 할당 연산자

---

`값이 할당되는 변수(상수)` = `할당할 값`의 형식이다.

```swift
var x
let y = 10
y = y + 10 // y에 y+10(20) 할당
```

### 산술 연산자

---

`-` (단항) | 변수 또는 표현식의 값을 음수로 만든다.
`*` | 곱셈
`//` | 나눗셈
`+` | 덧셈
`-` | 뺄셈
`%` | 나머지

### 복합 할당 연산자

---

`x += y` | `x = x + y`와 같은 의미
`x -= y` | `x = x - y`와 같은 의미
`x *= y` | `x = x * y`와 같은 의미
`x /= y` | `x = x / y`와 같은 의미
`x %= y` | `x = x % y`와 같은 의미
`x &= y` | x와 y의 bit AND 연산 결과를 x에 할당한다.
`x |= y` | x와 y의 bit OR 연산 결과를 X에 할당한다.

### 증가 연산자, 감소 연산자

---

```swift
// x의 값을 1 증가시킨다.
x = x + 1
x += 1
// x의 값을 1 감소시킨다.
x = x - 1 
x -= 1
```

Swift3 이전에는 `x++`나 `x--`도 사용이 가능했지만 Swift3에서 없어졌다.

따라서 현재는 `+`나 `+=`을 써주어야 한다.

### 비교 연산자

---

`x > y` | x가 y보다 크면 true를 반환한다.
`x >= y` | x가 y보다 크거나 같다면 true를 반환한다.
`x < y` | x가 y보다 작다면 true를 반환한다.
`x <= y` | x가 y보다 작거나 같다면 true를 반환한다.
`x != y` | x와 y가 같지 않다면 true를 반환한다.
`x == y` | x와 y가 (값이) 같다면 true를 반환한다.
`x === y` | x와 y가 (주소가) 같다면 true를 반환한다.

### 불리언 논리 연산자

---

`!` | NOT(불리언 값 또는 표현식의 결과를 반대로 바꾼다.)
`&&` | AND
`||` | OR
`^` | XOR

### 범위 연산자

---




**Notice:** 이 게시물은 Smile Han님의 유튜브와 developer.apple.com사이트를 참고하였습니다.<br>
[https://www.youtube.com/channel/UCM8wseo6DkA-D7yGlCrcrwA](https://www.youtube.com/channel/UCM8wseo6DkA-D7yGlCrcrwA "Smile Han님 유튜브")<br>
[https://developer.apple.com/documentation/swift/swift_standard_library/operator_declarations/](https://developer.apple.com/documentation/swift/swift_standard_library/operator_declarations/)
{: .notice--info}


