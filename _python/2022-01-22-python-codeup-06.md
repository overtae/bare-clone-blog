---
title: "[파이썬 기초 100제] 5강 산술연산"
date: 2022-01-22
categories:
  - Python
tags:
  - python
  - 기초 100제
  - 코드업
---

> 문제 38

<div class="notice--success" markdown="1">
**38.**   
정수 2개를 입력받아 합을 출력하는 프로그램을 작성해보자.
</div>

<div class="notice" markdown="1">
**풀이**

```python

```
</div>

> 문제 39

<div class="notice--success" markdown="1">
**39.**   
정수 2개를 입력받아 합을 출력하는 프로그램을 작성해보자.
</div>

<details>
<summary>참고</summary>
<div markdown="1">

실제 문제에서는 굉장히 넓은 정수 범위의 데이터형을 요구하는 문제이나 파이썬에서는 int()로 처리가 가능하다.

예를 들어 C에서 unsinged int보다도 크며 unsinged long과 같은 범위를 지니고 있다고 한다.

**실제 범위** : -9223372036854775808 ~ 9223372036854775807

이보다 큰 범위를 지정하고자 할 때는 long 데이터 형을 이용하면 된다.

파이썬에서는 4가지의 데이터형을 제공한다.

- int (plain integers) : 정수

- long (long integers) : int 보다 범위가 큰 정수

- float (floating point numbers) : 실수

- complex (complex numbers) : 복소수

</div>
</details>

<div class="notice" markdown="1">
**풀이**

```python

```
</div>

> 문제 40

<div class="notice--success" markdown="1">
**40.**   
입력된 정수의 부호를 바꿔 출력해보자.
</div>

<div class="notice" markdown="1">
**풀이**

```python

```
</div>

> 문제 41

<div class="notice--success" markdown="1">
**41.**   
영문자 1개를 입력받아 그 다음 문자를 출력해보자.<br>
영문자 'A'의 다음 문자는 'B'이고, 영문자 '0'의 다음 문자는 '1'이다.
</div>

<details>
<summary>TIP</summary>
<div markdown="1">

아스키 코드를 이용하면 된다.

'A' == 97(1000001), 'B' == 98(1000010) 이므로 아스키 코드로 변환된 숫자에 1을 더한 뒤 아스키 문자로 재변환 해주면 된다.

</div>
</details>

<div class="notice" markdown="1">
**풀이**

```python

```
</div>

> 문제 42

<div class="notice--success" markdown="1">
**42.**   
정수 2개(a, b) 를 입력받아 a를 b로 나눈 몫을 출력해보자.
</div>

<details>
<summary>TIP</summary>
<div markdown="1">

산술 연산자 '/'는 정확히 나눈 후의 값을 반환한다. ex) 1/3 >> 0.33333

산술 연산자 '//'는 나눈 후의 몫만 반환한다. ex) 1/3 >> 0

</div>
</details>

<div class="notice" markdown="1">
**풀이**

```python

```
</div>

> 문제 43

<div class="notice--success" markdown="1">
**43.**   
정수 2개(a, b) 를 입력받아 a를 b로 나눈 나머지를 출력해보자.
</div>

<div class="notice" markdown="1">
**풀이**

```python

```
</div>

> 문제 44

<div class="notice--success" markdown="1">
**44.**   
정수를 1개 입력받아 1만큼 더해 출력해보자.
</div>

<div class="notice" markdown="1">
**풀이**

```python

```
</div>

> 문제 45

<div class="notice--success" markdown="1">
**45.**   
정수 2개(a, b)를 입력받아 합, 차, 곱, 몫, 나머지, 나눈 값을 자동으로 계산해보자.

```
첫 줄에 합  
둘째 줄에 차,  
셋째 줄에 곱,  
넷째 줄에 몫,  
다섯째 줄에 나머지,  
여섯째 줄에 나눈 값을 순서대로 출력한다.  
(실수, 소수점 이하 셋째 자리에서 반올림해 둘째 자리까지 출력)  
```
</div>

<div class="notice" markdown="1">
**풀이**

```python

```
</div>

> 문제 46

<div class="notice--success" markdown="1">
**46.**   
정수 3개를 입력받아 합과 평균을 출력해보자.

```
합과 평균을 줄을 바꿔 출력한다.
평균은 소수점 이하 둘째 자리에서 반올림해서 소수점 이하 첫째 자리까지 출력한다.
```
</div>

<div class="notice" markdown="1">
**풀이**

```python

```
</div>

**Notice:** 이 게시물은 [우리밋_woorimIT](https://www.youtube.com/watch?v=7sykajCtgCw&list=PLSK4WsJ8JS4dOszA7Zr8paqI81Mv27tNq&index=2)님의 유튜브를 참고하였습니다.
{: .notice--info}