---
title: "[파이썬 프로그래머스] 문자열 내림차순으로 배치하기"
date: 2022-08-12
categories:
  - Python Programmers
tags:
  - python
  - 프로그래머스
---

### ❓ 문제

---

문자열 s에 나타나는 문자를 큰것부터 작은 순으로 정렬해 새로운 문자열을 리턴하는 함수, solution을 완성해주세요.

s는 영문 대소문자로만 구성되어 있으며, 대문자는 소문자보다 작은 것으로 간주합니다.


#### > &nbsp;제한 조건

---

- str은 길이 1 이상인 문자열입니다.


### ✔️ 풀이

---

{% highlight python linenos %}

def solution(s):
    return ''.join(sorted(s, reverse=True))

{% endhighlight %}


**Notice:** 이 게시물은 [programmers.co.kr](https://programmers.co.kr/learn/courses/30/lessons/12917) 사이트를 참고하였습니다.
{: .notice--info}