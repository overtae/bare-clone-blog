---
title: "[파이썬 코딩 도장] Unit 19 문제 풀이"
date: 2022-01-14
categories:
  - Python
tags:
  - python
  - 코딩 도장
excerpt: 계단식으로 별 출력하기
---

<div class="notice--danger" markdown="1">
**19.5 연습 문제 :**

다음 소스 코드를 완성하여 역삼각형 모양으로 별이 출력되게 만드세요.

```python
for i in range(5):
  for j in range(5):
    _________________________________
    ...
    _________________________________
  print()
# 결과 : 
# *****
#  ****
#   ***
#    **
#     *
```
</div>

<div class="notice" markdown="1">
**풀이**

```python
if j < i: # 나의 답 : if j > i (삼각형 모양으로 별이 출력)
  print(' ', end='')
else:
  print('*', end='')
```
공백이 세로줄에 비례하므로 j가 i보다 작을 때 공백 출력, 같거나 클 때 별을 출력해주어야 한다.
</div>

<div class="notice--danger" markdown="1">
**19.6 심사 문제 :**

표준 입력으로 삼각형의 높이가 입력됩니다.<br>
입력된 높이만큼 산 모양으로 별을 출력하는 프로그램을 만드세요.<br>
(input에서 안내 문자열은 출력하지 않아야 합니다)<br>
이때 출력 결과는 예제와 정확히 일치해야 합니다.<br>
모양이 같더라도 공백이나 빈 줄이 더 들어가면 틀린 것으로 처리됩니다.

```python
# 입력 : 3
# 결과 : 
#   *
#  ***
# *****
```
</div>

<div class="notice" markdown="1">
**풀이**

```python
# 답
h = int(input())
for i in range(h):
  for j in reversed(range(h)):
      if j > i:
          print(' ', end='')
      else:
          print('*', end='')
  for j in range(h):
      if j < i:
          print('*', end='')
  print()
# 나의 답
h = int(input())
for i in range(h):
  for j in i * 2: # TypeError: 'int' object is not iterable
    if j < i:
      print(' ', end='')
    else:
      print('*', end='')
  print()
```
분명 C언어에서 같은 지문을 봤었던 것 같은데 까먹었다. 위의 에러는 정수형은 순차적인 접근이 불가하다는 의미로 range(i * 2)로 바꿔주면 해결이 되긴 하지만 삼각형으로 출력이 되진 않는다.<br>
왼편과 오른편을 나눠서 생각해야했다.
</div>

**Notice:** 이 게시물은 파이썬 코딩 도장 사이트를 참고하였습니다.
[https://dojang.io/course/view.php?id=7](https://dojang.io/course/view.php?id=7)
{: .notice--info}