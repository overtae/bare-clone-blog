---
classes: wide
author_profile: true
title: "[Swift 문법 정리] 제어문"
date: 2022-01-08
categories:
  - Swift
tags:
  - swift
  - for-in
  - while
  - repeat-while
toc: true
toc_label: "목차"
toc_icon: bars
toc_sticky: true
---

### 조건-증가 for문(없어진 문법)

---

보통 for를 이용해 반복문을 만들 때 `for var i=0; i<10; i+=1 { }` 이런 식으로 할 것이다.

하지만 위와 같은 문법은 Swift 3에서 없어졌기 때문에 현재는 `for i in 0..<10 { }`으로 써주어야 한다.

### for-in 반복문

---

for-in 반복문은 컬렉션 또는 숫자 범위 내에 있는 목록을 반복하며 형식은 아래와 같다.

{% highlight swift linenos %}
import Foundation

for [상수명] in [컬렉션 또는 범위] {
    // 실행될 코드
    // [상수명]에는 [컬렉션 또는 범위]에서 가져온 항목이 할당된다.
}

for index in 1...3 {
    print(index)
}
// 1
// 2
// 3
{% endhighlight %}

#### _을 이용한 참조체(i)의 생략

만약 반복문 안에서 참조체가 사용될 일이 없다면 '_'을 사용해 생략해도 된다.

```swift
for _ in 1...3 { // swift에서 '_'는 무시를 의미
  print("만두")
} // 만두를 출력하는 걸 3번 반복
```

#### 배열의 항목 접근

```swift
let myAnimal = ["Dog", "Cat", "Zebra", "Tiger"] // 상수 배열

for animal in myAnimal {
    print(animal, terminator : " ")
}
// Dog Cat Zebra Tiger
```

<div class="notice--primary" markdown="1">
**terminator가 뭘까?** print()가 끝날 때 무엇으로 마칠지를 정해주는 인자로 기본값이 개행(\n)으로 되어있다. 그렇기 때문에 따로 써주지 않는다면 위의 소스는 총 4줄로 출력이 될 것이다. 위에선 이를 공백(" ")으로 바꿔주었기 때문에 한 줄로 출력이 되었다. print() 함수에 관한 자세한 설명은 [developer.apple.com](https://developer.apple.com/documentation/swift/1541053-print) 사이트를 참고하면 된다.
</div>

#### dictionary의 항목 접근

```swift
let numberOfFruits = ["apple": 10, "orange": 2, "grapefruit": 4] // dictionary는 [key: value] 형식의 배열이다.

for (fruit, amount) in numberOfFruits {
  print("I have \(amount) \(fruit)s")
}
// I have 2 oranges
// I have 10 apples
// I have 4 grapefruits
```

### while 반복문

---

`for-in`으로도 반복을 할 수 있는데 왜 while문이 있는걸까.

`for-in`은 *반복 횟수*를 아는 경우에 사용하기 적합하고 while문은 *반복 조건*을 아는 경우에 적합하다.

즉, while문은 지정된 조건을 만족할 때까지 작업을 반복한다.

```swift
while 조건식 {
  // 반복할 코드
}

var sum = 0

while sum < 100 { // 100이 되는 순간 조건에 맞지 않아 while을 빠져나간다.
  sum += 1
}
print(sum) // 100
```

### repeat-while 반복문

---

while 반복문을 사용했을 때 처음부터 조건에 맞지 않는다면 반복문을 바로 빠져나갈 것이다.

하지만 repeat-while 반복문을 사용하면 조건에 맞지 않더라도 적어도 한번은 실행된다.

```swift
repeat {
  // 반복할 코드(적어도 한번은 실행할 코드)
} while 조건식

var sum = 0

repeat {
  sum += 1
} while sum < 100

print(sum) // 100
```



**Notice:** 이 게시물은 Smile Han님의 유튜브를 참고하였습니다.<br>
[https://www.youtube.com/channel/UCM8wseo6DkA-D7yGlCrcrwA](https://www.youtube.com/channel/UCM8wseo6DkA-D7yGlCrcrwA "Smile Han님 유튜브")
{: .notice--info}