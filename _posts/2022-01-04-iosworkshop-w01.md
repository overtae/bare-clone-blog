---
title: "[Swift 문법 정리] "
date: 2022-01-04
categories:
  - Swift
tags:
  - iOS
  - swift
---

{ % highlight swift lineos % }
```swift
var x = 10
while true {
    guard x > 0 else { break } // x > 0이 거짓일 때 실행
    print(x, terminator:" ") // 10 8 6 4 2
    x -= 2
}
```
{ % endhighlight % }


**Notice:** 이 게시물은 Smile Han님의 유튜브를 참고하였습니다.
https://www.youtube.com/channel/UCM8wseo6DkA-D7yGlCrcrwA
{: .notice--info}