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
**5.5 연습 문제:** 

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

> Unit 6 문제 풀이

<div class="notice--success" markdown="1">
**6.6 연습 문제 :** 

다음 소스 코드를 완성하여 정수 세 개를 입력받고 합계가 출력되게 만드세요.

```python
_________________________
print(a + b + c)
# 입력 : -10 20 30
# 결과 : 40
```
</div>

<div class="notice" markdown="1">
**풀이** 

```python
a, b, c = map(int, input().split())
```
</div>

<div class="notice--warning" markdown="1">
**6.7 심사 문제 :** 

다음 소스 코드를 완성하여 50, 100, None이 각 줄에 출력되게 만드세요.

```python
_____________
_____________
_____________

print(a)
print(b)
print(c)
# 결과 : 
# 50
# 100
# None
```
</div>

<div class="notice" markdown="1">
**풀이** 

```python
a = 50
b = 100
c = 'None'
```
`a, b, c = 50, 100, None` 이렇게 한 줄로 값을 할당하는 방법도 있다.
</div>

<div class="notice--warning" markdown="1">
**6.8 심사 문제 :** 

표준 입력으로 국어, 영어, 수학, 과학 점수가 입력됩니다.<br>
평균 점수를 출력하는 프로그램을 만드세요(input에서 안내 문자열은 출력하지 않아야 합니다).<br>
단, 평균 점수를 출력할 때는 소수점 이하 자리는 버립니다(정수로 출력).

```python
________________
________________

# 입력 : 83 92 87 90
# 결과 : 88
```
</div>

<div class="notice" markdown="1">
**풀이** 

```python
a, b, c, d = map(int, input().split())
print(int((a + b + c + d) / 4))
```
`(a + b + c + d) // 4`<br>
int()를 사용하지 않고 버림 나눗셈 연산자(//)를 사용하는 방법도 있다.
</div>

> Unit 7 문제 풀이

<div class="notice--success" markdown="1">
**7.4 연습 문제 :** 

다음 소스 코드를 완성하여 날짜와 시간이 출력되게 만드세요.

```python
year = 2000
month = 10
day = 27
hour = 11
minute = 43
second = 59
 
print(year, month, day, ________________)
print(hour, minute, second, ________)
# 결과 : 2000/10/27 11:43:59
```
</div>

<div class="notice" markdown="1">
**풀이** 

`sep = '/', end = ''`<br>
`sep = ':'`
</div>

<div class="notice--danger" markdown="1">
**7.5 심사 문제:** 

표준 입력으로 년, 월, 일, 시, 분, 초가 입력됩니다.<br>
다음 소스 코드를 완성하여 입력된 날짜와 시간을 년-월-일T시:분:초 형식으로 출력되게 만드세요.

```python
year, month, day, hour, minute, second = input().split()

_______________________________________
print(hour, minute, second, sep=':')
# 입력 : 1999 12 31 10 37 21
# 결과 : 1999-12-31ㅆ10:37:21
```
</div>

<div class="notice" markdown="1">
**풀이** 

```python
print(year, month, day, sep='-', end='T')
```
처음에 `sep:'-'` 이렇게 적었다. 꼭 등호를 사용하자..
</div>

> Unit 8 문제 풀이

<div class="notice--danger" markdown="1">
**8.4 연습 문제:** 

국어, 영어, 수학, 과학 점수가 있을 때 한 과목이라도 50점 미만이면 불합격이라고 정했습니다.<br>
다음 소스 코드를 완성하여 합격이면 True, 불합격이면 False가 출력되게 만드세요.

```python
korean = 92
english = 47
mathematics = 86
science = 81
 
print(___________________________)
# 결과 : False
```
</div>

<div class="notice" markdown="1">
**풀이** 

`korean >= 50 and english >= 50 and mathematics >= 50 and science >= 50`<br>
`&&`를 적었었는데 오류가 났다. 꼭 `and`를 사용하자.
</div>

<div class="notice--success" markdown="1">
**8.5 심사 문제 :** 

표준 입력으로 국어, 영어, 수학, 과학 점수가 입력됩니다.<br>
국어는 90점 이상, 영어는 80점 초과, 수학은 85점 초과, 과학은 80점 이상일 때 합격이라고 정했습니다.<br>
(한 과목이라도 조건에 만족하지 않으면 불합격)<br>
다음 소스 코드를 완성하여 합격이면 True, 불합격이면 False가 출력되게 만드세요.<br>
(input에서 안내 문자열은 출력하지 않아야 합니다)

```python
________________
________________
# 입력 : 90 81 86 80
# 결과 : True
```
</div>

<div class="notice" markdown="1">
**풀이** 

```python
a, b, c, d = map(int, input().split())
print(a >= 90 and b > 80 and c > 85 and d >= 80)
```
</div>

> Unit 9 문제 풀이

<div class="notice--success" markdown="1">
**9.3 연습 문제 :** 

다음 소스 코드를 완성하여 실행 결과대로 문자열이 출력되게 만드세요.

```python
s = _______________________
___________________________
___________________________
print(s)
# 결과 :
# Python is a programming language that lets you work quickly
# and
# integrate systems more effectively.
```
</div>

<div class="notice" markdown="1">
**풀이** 

`"""Python is a programming language that lets you work quickly`<br>
`and`<br>
`integrate systems more effectively."""`
</div>

<div class="notice--success" markdown="1">
**9.4 심사 문제 :** 

다음 소스 코드를 완성하여 실행 결과대로 문자열이 출력되게 만드세요.

```python
____________________
____________________
____________________
print(s)
# 결과 :
# 'Python' is a "programming language"
# that lets you work quickly
# and
# integrate systems more effectively.
```
</div>

<div class="notice" markdown="1">
**풀이** 

```python
s = """'Python' is a "programming language"
that lets you work quickly
and
integrate systems more effectively."""
```
</div>

> Unit 10 문제 풀이

<div class="notice--success" markdown="1">
**10.4 연습 문제 :** 

다음 소스 코드를 완성하여 리스트 [5, 3, 1, -1, -3, -5, -7, -9]가 출력되게 만드세요.<br>
리스트를 만들 때는 range를 사용해야 합니다.

```python
__________range__________
 
print(a)
# 결과 : [5, 3, 1, -1, -3, -5, -7, -9]
```
</div>

<div class="notice" markdown="1">
**풀이** 

`a = list(range(5, -10, -2))`
</div>

<div class="notice--warning" markdown="1">
**10.5 심사 문제 :** 

표준 입력으로 정수가 입력됩니다.<br>
range의 시작하는 숫자는 -10, 끝나는 숫자는 10이며<br>
입력된 정수만큼 증가하는 숫자가 들어가도록 튜플을 만들고,<br>
해당 튜플을 출력하는 프로그램을 만드세요.<br>
(input에서 안내 문자열은 출력하지 않아야 합니다)

```python
___________________
___________________
___________________
# 입력 : 2
# 결과 : (-10, -8, -6, -4, -2, 0, 2, 4, 6, 8)
```
</div>

<div class="notice" markdown="1">
**풀이** 

```python
a = int(input())
b = tuple(range(-10, 10, a))
print(b)
```
`print(tuple(range(-10, 10, a)))` 이렇게 바로 출력하는 방법도 있다고 한다.
</div>

> Unit 11 문제 풀이

<div class="notice--success" markdown="1">
**11.6 연습 문제 :** 

리스트 year에 연도, population에 서울시 인구수가 저장되어 있습니다.<br>
다음 소스 코드를 완성하여 최근 3년간 연도와 인구수가 리스트로 출력되게 만드세요.<br>

```python
year = [2011, 2012, 2013, 2014, 2015, 2016, 2017, 2018]
population = [10249679, 10195318, 10143645, 10103233, 10022181, 9930616, 9857426, 9838892]
 
print(_________)
print(______________)
# 결과 :
# [2016, 2017, 2018]
# [9930616, 9857426, 9838892]
```
</div>

<div class="notice" markdown="1">
**풀이** 

`year[-3:]`<br>
`population[-3:]`
</div>

<div class="notice--danger" markdown="1">
**11.7 연습 문제 :** 

다음 소스 코드를 완성하여 튜플 n에서 인덱스가 홀수인 요소들이 출력되게 만드세요.<br>

```python
n = -32, 75, 97, -10, 9, 32, 4, -15, 0, 76, 14, 2
 
print(__________)
# 결과 : (75, -10, 32, -15, 76, 2)
```
</div>

<div class="notice" markdown="1">
**풀이** 

`n[1::2]`<br>
처음에 `n[::2]`라 했었는데 이건 인덱스가 짝수인 요소들이었다. 홀수는 1부터 시작, 2씩 증가한다는걸 기억하자.
</div>

<div class="notice--danger" markdown="1">
**11.8 심사 문제 :** 

표준 입력으로 숫자 또는 문자열 여러 개가 입력되어 리스트 x에 저장됩니다.<br>
(입력되는 숫자 또는 문자열의 개수는 정해져 있지 않음)<br>
다음 소스 코드를 완성하여 리스트 x의 마지막 요소 5개를 삭제한 뒤 튜플로 출력되게 만드세요.

```python
x = input().split()

________________
________________
# 입력 : 1 2 3 4 5 6 7 8 9 10
# 결과 : ('1', '2', '3', '4', '5')
```
</div>

<div class="notice" markdown="1">
**풀이** 

```python
# 답
del x[-5:]
print(tuple(x))
# 나의 답
y = tuple(del x[-5:])
print(y)
```

del은 tuple() 안에 사용하지 못한다는 걸 꼭 명심하자.
</div>

<div class="notice--danger" markdown="1">
**11.9 심사 문제 :** 

표준 입력으로 문자열 두 개가 각 줄에 입력됩니다.<br>
(문자열의 길이는 정해져 있지 않음)<br>
첫 번째 문자열에서 인덱스가 홀수인 문자와 두 번째 문자열에서 인덱스가 짝수인 문자를 연결하여 출력하는 프로그램을 만드세요.<br>
(input에서 안내 문자열은 출력하지 않아야 합니다)<br>
연결 순서는 첫 번째 문자열, 두 번째 문자열 순입니다.<br>
그리고 0은 짝수로 처리합니다.

```python
________________
________________
________________
# 입력 : 
# python
# python
# 결과 : yhnpto
```
</div>

<div class="notice" markdown="1">
**풀이** 

```python
# 답
a = input()
b = input()
print(a[1::2]+b[::2])
# 나의 답
a = input()
b = input()
print(a[1::2], b[::2])
```

문자를 연결한다는 건 + 연산자의 사용을 뜻한다는걸 기억하자.
</div>

> Unit 12 문제 풀이

<div class="notice--success" markdown="1">
**12.4 연습 문제 :** 

다음 소스 코드를 완성하여 게임 캐릭터의 체력(health)과 이동 속도(movement speed)가 출력되게 만드세요.

```python
camille = {
    'health': 575.6,
    'health_regen': 1.7,
    'mana': 338.8,
    'mana_regen': 1.63,
    'melee': 125,
    'attack_damage': 60,
    'attack_speed': 0.625,
    'armor': 26,
    'magic_resistance': 32.1,
    'movement_speed': 340
}
 
print(_______________)
print(_______________)
# 결과 : 
# 575.6
# 340
```
</div>

<div class="notice" markdown="1">
**풀이** 

`camille['health']`<br>
`camille['movement_speed']`
</div>

<div class="notice--success" markdown="1">
**12.5 연습 문제 :** 

표준 입력으로 문자열 여러 개와 숫자(실수) 여러 개가 두 줄로 입력됩니다.<br>
입력된 첫 번째 줄은 키, 두 번째 줄은 값으로 하여 딕셔너리를 생성한 뒤 딕셔너리를 출력하는 프로그램을 만드세요.<br>
input().split()의 결과를 변수 한 개에 저장하면 리스트로 저장됩니다.

```python
_______________
_______________
_______________
_______________
# 입력 : 
# health health_regen mana mana_regen
# 575.6 1.7 338.8 1.63
# 결과 : {'health': 575.6, 'health_regen': 1.7, 'mana': 338.8, 'mana_regen': 1.63}
```
</div>

<div class="notice" markdown="1">
**풀이** 

```python
a = input().split()
b = map(float, input().split())
c = dict(zip(a,b))
print(c)
```
</div>




**Notice:** 이 게시물은 파이썬 코딩 도장 사이트를 참고하였습니다.
[https://dojang.io/course/view.php?id=7](https://dojang.io/course/view.php?id=7)
{: .notice--info}
