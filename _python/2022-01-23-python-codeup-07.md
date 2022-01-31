---
permalink: /python/python-17/
classes: wide
title: "[파이썬 기초 100제] 6강 비트 시프트 연산"
date: 2022-01-23
categories:
  - Python
tags:
  - python
  - 기초 100제
  - 코드업
---

> 문제 47

<div class="notice--danger" markdown="1">
**47.**   
정수 1개를 입력받아 2배 곱해 출력해보자.
</div>

<details>
<summary>TIP</summary>
<div markdown="1">

곱하기 2를 해도 되지만 이진수를 왼쪽으로 한 번씩 이동시켜주면 기존 값의 두 배가 된다.

ex) 5(101) => 10(1010), 7(111) => 14(1110)

</div>
</details>

<div class="notice" markdown="1">
**풀이**

```python
# 답
x = int(input())
print( x<<1 )
# 나의 답
x = int(input())
print(x * 2)
```
비트 시프트 연산은 왼쪽으로 이동시키는 `<<`와 오른쪽으로 이동시키는 `>>`라는걸 기억하자.
</div>

> 문제 48

<div class="notice--warning" markdown="1">
**48.**   
정수 2개(a, b)를 입력받아 a를 2(b 제곱)배 곱한 값으로 출력해보자. ( a * 2(b 제곱) )
</div>

<details>
<summary>TIP</summary>
<div markdown="1">

![image]({{ site.url }}{{ site.baseurl }}/assets/images/python/01.png){: .align-center}

</div>
</details>

<div class="notice" markdown="1">
**풀이**

```python
a, b = map(int, input().split())
print(a << b)
```
참고 사진이 없었다면 풀지 못했을 것이다.<br>
이제부터라도 알아두도록 하자.
</div>

**Notice:** 이 게시물은 [우리밋_woorimIT](https://www.youtube.com/watch?v=7sykajCtgCw&list=PLSK4WsJ8JS4dOszA7Zr8paqI81Mv27tNq&index=2)님의 유튜브를 참고하였습니다.
{: .notice--info}