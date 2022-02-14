---
permalink: /python/python-06/
title: "[파이썬 코딩 도장] Unit 16 문제 풀이"
date: 2022-01-13
categories:
  - Python dojang
tags:
  - python
  - 코딩 도장
excerpt: for 반복문 사용하기
---

<div class="notice--success" markdown="1">
**16.5 연습 문제 :**

다음 소스 코드를 완성하여 리스트 x에 들어있는 각 숫자(요소)에 10을 곱한 값이 출력되게 만드세요.<br>
모든 숫자는 공백으로 구분하여 한 줄로 출력되어야 합니다.

```python
x = [49, -17, 25, 102, 8, 62, 21]
_____________
  ______________________
# 결과 : 490 -170 250 1020 80 620 210 
```
</div>

<div class="notice" markdown="1">
**풀이**

```python
for i in x:
  print(i * 10, end=' ')
```
</div>

<div class="notice--success" markdown="1">
**16.6 심사 문제 :**

표준 입력으로 정수가 입력됩니다.<br>
입력된 정수의 구구단을 출력하는 프로그램을 만드세요.<br>
(input에서 안내 문자열은 출력하지 않아야 합니다)<br>
출력 형식은 숫자 * 숫자 = 숫자처럼 만들고 숫자와 *, = 사이는 공백을 한 칸 띄웁니다.

```python
________________
________________
________________
# 입력 : 2
# 결과 :
# 2 * 1 = 2
# 2 * 2 = 4
# ...
# 2 * 8 = 16
# 2 * 9 = 18
```
</div>

<div class="notice" markdown="1">
**풀이**

```python
x = int(input())
for i in range(1, 10):
  print(x, '*', i, '=', x * i)
```
처음엔 `x*i`라 적었지만, `*` 양 옆 공간은 한 칸씩 띄우는 게 좋을 것 같다.
</div>

<details>
<summary>PEP 8 - Whitespace in operators</summary>
<div markdown="1">       

`If operators with different priorities are used, consider adding whitespace around the operators with the lowest priority(ies).`

```python
# Correct:
i = i + 1
submitted += 1
x = x*2 - 1
hypot2 = x*x + y*y
c = (a+b) * (a-b)

# Wrong:
i=i+1
submitted +=1
x = x * 2 - 1
hypot2 = x * x + y * y
c = (a + b) * (a - b)
```
**원문 :** [Style Guide for Pyhton Code](https://www.python.org/dev/peps/pep-0008/#other-recommendations)
{: .notice--info}

</div>
</details>

**Notice:** 이 게시물은 파이썬 코딩 도장 사이트를 참고하였습니다.
[https://dojang.io/course/view.php?id=7](https://dojang.io/course/view.php?id=7)
{: .notice--info}