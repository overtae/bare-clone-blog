---
permalink: /python/python-14/
title: "[파이썬 기초 100제] 3강 데이터형"
date: 2022-01-20
categories:
  - Python
tags:
  - python
  - 기초 100제
  - 코드업
---

> 문제 28

<div class="notice--success" markdown="1">
**28.**   
정수 1개를 입력받아 그대로 출력해보자.
</div>

<details>
<summary>파이썬에서 제공하는 데이터형</summary>
<div markdown="1">

파이썬에서의 int() 데이터형의 크기는 4바이트(32비트)로 지정되어있다.

이보다 큰 범위를 지정하고자 할 때는 long 데이터 형을 이용하면 된다.

파이썬에서는 4가지의 데이터형을 제공한다.

- int (plain integers) : 정수

- long (long integers) : int 보다 범위가 큰 정수(메모리 한계까지 저장 가능, 사실상 무제한)

- float (floating point numbers) : 실수

- complex (complex numbers) : 복소수

</div>
</details>

<div class="notice" markdown="1">
**풀이**

```python
x = int(input())
print(x)
```
</div>

> 문제 29

<div class="notice--success" markdown="1">
**29.**   
실수 1개를 입력받아 그대로 출력해보자.
</div>

<div class="notice" markdown="1">
**풀이**

```python
x = float(input())
print(x)
```
</div>

> 문제 30

<div class="notice--success" markdown="1">
**30.**   
정수 1개를 입력받아 그대로 출력해보자.
</div>

<div class="notice" markdown="1">
**풀이**

```python
x = int(input())
print(x)
```
</div>

**Notice:** 이 게시물은 [우리밋_woorimIT](https://www.youtube.com/watch?v=7sykajCtgCw&list=PLSK4WsJ8JS4dOszA7Zr8paqI81Mv27tNq&index=2)님의 유튜브를 참고하였습니다.
{: .notice--info}