---
title: "[Swift 문법 정리] 자료형(데이터 타입)"
date: 2022-01-04
categories:
  - Swift
tags:
  - iOS
  - swift
toc: true
toc_label: "목차"
toc_icon: bars
toc_sticky: true
---

#### 자료형의 종류

Int | Integer의 약자, 정수(음수, 0, 양수)
UInt | Unsigned Integer의 약자, 부호가 없는 정수(0, 양수)
Float | 실수(6자리)
Double | 실수(15자리)
Character | 문자
String | 문자열
Bool | 참과 거짓
Void | 값이 없음(주의: 0이 아님)

#### 숫자를 저장하는 방법

스위프트에서 값을 저장하는 방법으로 상수(let), 변수(var)가 있다.
형식은 아래와 같다.

변수 | var [변수명] : [자료형] = [값]
상수 | let [상수명] : [자료형] = [값]

```swift
var x = 10 // 변수 선언
let y = 20 // 상수 선언

var z : Int // 콜론 뒤에 자료형을 적어준다. 이때, 자료형은 대문자로 시작한다.
z = 10
```

초깃값이 있을 경우 컴파일러가 자료형이 뭔지 인식(타입 추론: type inference)을 하기 때문에 자료형(: Int) 생략이 가능하다.
추가로 세미콜론(;)도 따로 적어주지 않아도 된다.

> 주의

```swift
var x= 10
// error '=' must have consistent whitespace on both sides
// '=' 양쪽에 동일한 공백이 필요하다
```

위와 같이 등호(=) 양쪽으로 다른 공백이 입력되어 있다면 에러가 나게 된다. 꼭 동일한 공백을 입력하도록 하자.


**Notice:** 이 게시물은 Smile Han님의 유튜브를 참고하였습니다.
[https://www.youtube.com/channel/UCM8wseo6DkA-D7yGlCrcrwA](https://www.youtube.com/channel/UCM8wseo6DkA-D7yGlCrcrwA)
{: .notice--info}