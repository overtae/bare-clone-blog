---
title: "[파이썬 코딩 도장] Unit 3 ~ Unit 12 문제 풀이"
date: 2022-01-05
categories:
  - Python
tags:
  - python
  - 코딩 도장
---

> Unit 3 문제 풀이

<div class="notice--success" markdown="1">
**3.7 연습 문제 :** 

다음 소스 코드를 완성하여 'Hello, world!'와 'Python Programming'이 각 줄에 출력되게 만드세요. 

```python
print('Hello, world!')
print(_______________)
```
</div>

<div class="notice" markdown="1">
**풀이** 

`'Python Programming'`
</div>

<div class="notice--success" markdown="1">
**3.8 심사 문제 :** 

'Hello, world!' 두 개를 각 줄에 출력하는 프로그램을 만드세요.<br>
(대소문자 구분과 띄어쓰기가 정확해야 합니다)<br>
정답에는 출력 결과를 만족하는 전체 소스 코드를 입력해야 합니다.
</div>

<div class="notice" markdown="1">
**풀이** 

```python
print('Hello, world!')
print('Hello, world!')
```
</div>

> Unit 5 문제 풀이

<div class="notice--danger" markdown="1">
**5.5 연습문제:** 

아파트에서 소음이 가장 심한 층수 출력하기<br>
국립환경과학원에서는 아파트에서 소음이 가장 심한 층수를 구하는 계산식을 발표했습니다.<br>
소음이 가장 심한 층은 0.2467 * 도로와의 거리(m) + 4.159입니다.<br>
다음 소스 코드를 완성하여 소음이 가장 심한 층수가 출력되게 만드세요.<br>
단, 층수를 출력할 때는 소수점 이하 자리는 버립니다(정수로 출력).<br>
- 도로와의 거리: 12m

```python
print(_______________)
# 결과 : 7
```
</div>

<div class="notice" markdown="1">
**풀이** 

`int(0.2467 * 12 + 4.159)`<br>
처음에 Int라 적었는데 오류가 났다. 꼭 int라 적도록 하자.
</div>

<div class="notice--success" markdown="1">
**5.6 심사 문제 :** 

L이라는 게임에서 "왜곡"이라는 스킬이 AP * 0.6 + 225의 피해를 입힙니다.<br>
참고로 이 게임에서 AP(Ability Power, 주문력)는 마법 능력치를 뜻합니다.<br>
다음 소스 코드를 완성하여 스킬의 피해량이 출력되게 만드세요.<br>
- AP: 102

```python
print(102 ________)
# 결과 : 286.2
```
</div>

<div class="notice" markdown="1">
**풀이** 

`* 0.6 + 225`
</div>



**Notice:** 이 게시물은 파이썬 코딩 도장 사이트를 참고하였습니다.
[https://dojang.io/course/view.php?id=7](https://dojang.io/course/view.php?id=7)
{: .notice--info}
