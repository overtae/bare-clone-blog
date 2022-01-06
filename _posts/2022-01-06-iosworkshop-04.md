---
title: "[Swift 문법 정리] Any와 AnyObject"
date: 2022-01-06
categories:
  - Swift
tags:
  - swift
  - Any
  - AnyObject
toc: true
toc_label: "목차"
toc_icon: bars
toc_sticky: true
---

### AnyObject란?

---

AnyObject는 프로토콜(protocol)로 어떠한 **클래스**의 인스턴스도 저장이 가능한 범용 타입이다.

클래스만 허용하며 구조체나 열거형은 허용하지 않는다.

**프로토콜이란?** 클래스의 가장 추상화 된 최상위 개념이다.
{: .notice--primary}

### Any란?

---

AnyObject가 클래스의 인스턴스만 저장이 가능하다면 Any는 클래스, 구조체, 열거형, 함수타입도 저장이 가능하다.


**Notice:** 이 게시물은 Smile Han님의 유튜브를 참고하였습니다.
[https://www.youtube.com/channel/UCM8wseo6DkA-D7yGlCrcrwA](https://www.youtube.com/channel/UCM8wseo6DkA-D7yGlCrcrwA)
{: .notice--info}