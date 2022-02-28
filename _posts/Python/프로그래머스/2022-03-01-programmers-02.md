---
title: "[파이썬 프로그래머스] 짝수와 홀수"
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

정수 num이 짝수일 경우 "Even"을 반환하고 홀수인 경우 "Odd"를 반환하는 함수, solution을 완성해주세요.

> 제한 사항

- num은 int 범위의 정수입니다.
- 0은 짝수입니다.

> 입출력 예

num | return
--- | ---
3 | "Odd"
4 | "Even"

### 풀이

---

{% highlight python linenos %}
def solution(num):
    return "Odd" if num % 2 else "Even"
{% endhighlight %}

**Notice:** 이 게시물은 [programmers.co.kr](https://programmers.co.kr/learn/courses/30/lessons/12937) 사이트를 참고하였습니다.
{: .notice--info}