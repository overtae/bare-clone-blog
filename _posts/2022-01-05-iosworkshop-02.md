---
title: "[Swift 문법 정리] 옵셔널(optional)"
date: 2022-01-05
categories:
  - Swift
tags:
  - swift
  - optional
  - 옵셔널
  - 옵셔널 바인딩
toc: true
toc_label: "목차"
toc_icon: bars
toc_sticky: true
---

### 옵셔널(Optional)이란?

---

옵셔널 타입에 관해 설명하기 앞서 10과 Optional(10)의 차이가 무엇일까. 

10은 그 값 자체로 연산이 가능하지만 Optional(10)은 옵셔널을 풀어주어야 연산이 가능하다.

그렇다면 옵셔널을 쓰는 이유는 무엇일까.

옵셔널은 일반적인 값 이외에도 nil(값이 없음)을 저장할 수 있기 때문이다.

변수 또는 상수에 아무런 값이 할당되지 않는 경우에 오류가 발생할 수 있기 때문에 옵셔널이라는 데이터 타입으로 감싸주어 안전하게 반환을 하게 된다.

```swift
// 괄호 안의 문자열을 Int형으로 변환해주는 Int()
// 자료형의 경우 구조체로 되어있어 괄호를 열게 되면 initializer가 호출된다.
print(Int("10")) // Optional(10)
print(Int("H")) // nil
```

위의 소스를 실행해보면 경고 메세지가 뜨긴 하지만 값이 출력되긴 한다.

10은 정수형으로 변환이 가능하기 때문에 문제가 없었지만, 문자 'H'를 정수형으로 변환하려고 하면 문제가 된다.

따라서 Int형 initializer가 리턴값을 옵셔널로 감싸서 숫자가 아닌 문자를 받았을 때 안전하게 nil을 반환하도록 한 것이다.

옵셔널 타입은 정말 많은 곳에 사용되기 때문에 꼭 알아두어야 한다.

### 옵셔널 변수 선언

---

옵셔널 변수를 선언하고 싶다면 자료형 뒤에 물음표(?)나 느낌표(!)를 써주면 된다.

```swift
var optionalInt : Int? // Optional Int형 
let optionalDouble : Double? // Optional Double형 
let optionalString : String? // Optinal String형 

print(optionalInt) // nil, 초기값을 안주었을 경우 nil이 초기값이 된다.
optionalInt = 10
print(optionalInt) // Optional(10)

optionalInt = optionalInt + 2 // 오류, 옵셔널값과 정수값은 연산이 불가하다.
var x : Int = optionalInt // 오류, 옵셔널 변수의 값은 정수형 변수에 저장이 불가하다.
```

옵셔널 변수를 선언하게 되면 정수형으로 10을 저장하고 싶어도 Optional(10)으로 저장된다.

### 옵셔널 강제 언래핑(forced unwrapping)

---

옵셔널로 감싸진(wrapped) 변수 또는 상수를 풀고 싶다면 어떻게 해야 할까.

가장 간단한 방법으로는 변수나 상수 뒤에 느낌표(!)를 붙이는 것이다.

하지만 이 방법의 경우 nil을 언래핑 하려고 했을 때 오류가 발생하기 때문에 값이 항상 존재할 것이라 확신하는 경우에만 사용해야 한다.

따라서 if문을 사용해 nil이 아닐때만 옵셔널을 풀게끔 해주어 오류를 방지할 수 있다.

```swift
var optionalInt : Int? = 10

print(optionalInt) // Optional(10)
print(optionalInt!) // 10, forced unwrapping
```

```swift
var x : Int?
x = 10
if x != nil {
    print(x!) // x의 값이 존재하면 옵셔널을 풀어 그 값을 출력한다.
} else {
    print("값이 없습니다.") // x의 값이 없다면 "값이 없습니다."를 출력한다.
}
// 실행 결과는 10
```

<div class="notice--danger" markdown="1">
**주의** `if x!=nil` 또는 `if x!= nil`이라 썼을 경우 <span style="color:red">error:</span> 'nil' cannot be assigned to type 'Int'라는 에러가 나게 된다. 간격에 주의하도록 하자.
</div>





**Notice:** 이 게시물은 Smile Han님의 유튜브를 참고하였습니다.
[https://www.youtube.com/channel/UCM8wseo6DkA-D7yGlCrcrwA](https://www.youtube.com/channel/UCM8wseo6DkA-D7yGlCrcrwA)
{: .notice--info}