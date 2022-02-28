---
title: "[파이썬 프로그래머스] 문자열 내 p와 y의 개수"
date: 2022-03-01
categories:
  - Python Programmers
tags:
  - python
  - 프로그래머스
  - 레벨 1
---

### 문제

---

대문자와 소문자가 섞여있는 문자열 s가 주어집니다. s에 'p'의 개수와 'y'의 개수를 비교해 같으면 True, 다르면 False를 return 하는 solution를 완성하세요.

'p', 'y' 모두 하나도 없는 경우는 항상 True를 리턴합니다.

단, 개수를 비교할 때 대문자와 소문자는 구별하지 않습니다.

예를 들어 s가 "pPoooyY"면 true를 return하고 "Pyy"라면 false를 return합니다.

> 제한 사항
- 문자열 s의 길이 : 50 이하의 자연수
- 문자열 s는 알파벳으로만 이루어져 있습니다.

> 입출력 예
s | answer | 설명
--- | --- | ---
"pPoooyY" | true | 'p'의 개수 2개, 'y'의 개수 2개로 같으므로 true를 return 합니다.
"Pyy" | false | 'p'의 개수 1개, 'y'의 개수 2개로 다르므로 false를 return 합니다.

### 풀이

---

{% highlight python linenos %}
def solution(s):
    answer = True
    p = 0
    y = 0
    
    for i in s:
        if i == 'p' or i == 'P':
            p += 1
        if i == 'y' or i == 'Y':
            y += 1
    
    if p != y:
        answer = False

    return answer
{% endhighlight %}

**Notice:** 이 게시물은 [programmers.co.kr](https://programmers.co.kr/learn/courses/30/lessons/12916) 사이트를 참고하였습니다.
{: .notice--info}