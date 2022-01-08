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
  - break
  - continue
  - if
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

```swift
import Foundation

for [상수명] in [컬렉션 또는 범위] {
    // 실행될 코드
    // [상수명]에는 [컬렉션 또는 범위]에서 가져온 항목이 할당된다.
}

let myAnimal = ["Dog", "Cat", "Zebra", "Tiger"]

for animal in myAnimal {
    print(animal, terminator : " ")
}
// Dog Cat Zebra Tiger
```

<div class="notice--primary" markdown="1">
**terminator가 뭘까?** print()가 끝날 때 무엇으로 마칠지를 정해주는 인자로 기본값이 개행(\n)으로 되어있다. 그렇기 때문에 따로 써주지 않는다면 위의 소스는 총 4줄로 출력이 될 것이다. 위에선 이를 공백(" ")으로 바꿔주었기 때문에 한 줄로 출력이 되었다. print() 함수에 관한 자세한 설명은 [developer.apple.com](https://developer.apple.com/documentation/swift/1541053-print) 사이트를 참고하면 된다.
</div>








**Notice:** 이 게시물은 Smile Han님의 유튜브를 참고하였습니다.<br>
[https://www.youtube.com/channel/UCM8wseo6DkA-D7yGlCrcrwA](https://www.youtube.com/channel/UCM8wseo6DkA-D7yGlCrcrwA "Smile Han님 유튜브")
{: .notice--info}