---
title: "[파이썬 기초 100제] 2강 입출력 - 1"
date: 2022-01-18
categories:
  - Python
tags:
  - python
  - 기초 100제
  - 코드업
---

<div class="notice--success" markdown="1">
**10.**   
정수형(int)으로 변수를 선언하고, 변수에 정수값을 저장한 후 변수에 저장되어 있는 값을 그대로 출력해보자.
</div>

<div class="notice" markdown="1">
**풀이**

```python


```
</div>

<div class="notice--success" markdown="1">
**11.**   
문자형(char)으로 변수를 하나 선언하고, 변수에 문자를 저장한 후 변수에 저장되어 있는 문자를 그대로 출력해보자.
</div>

<details>
<summary>TIP</summary>
<div markdown="1">

`input()`의 반환값은 기본으로 문자열로 정의된다.

</div>
</details>

<div class="notice" markdown="1">
**풀이**

```python


```
</div>

<div class="notice--success" markdown="1">
**12.**   
실수형(float)로 변수를 선언하고 그 변수에 실수값을 저장한 후 저장되어 있는 실수값을 출력해보자.
</div>

<div class="notice" markdown="1">
**풀이**

```python


```
</div>

<div class="notice--success" markdown="1">
**13.**   
정수(int) 2개를 입력받아 그대로 출력해보자.<br>
(단, 띄어쓰기를 기준으로 입력한다.)<br>
입력 : 1 5<br>
출력 : 1 5
</div>

<details>
<summary>TIP</summary>
<div markdown="1">

문자열의 메소드(함수)인 `split()`을 이용하면 문자열을 공백 기준으로 배열(iterable)로 만들어준다.<br>

매핑함수인 map()을 이용하면 배열(iterable)의 모든 원소를 첫 번째 매개변수(parameter)로 변환할 수 있다. 정확히는 감싸준다는 표현이 맞다.<br>

ex ) `map(int, ['1', '2', '3']) >> [1,2,3]`<br>

매핑함수 `map()`의 반환값은 map객체이다. 따라서 육안으로 확인하기 위해서는 `list()`로 변환시켜줘야한다.

</div>
</details>

<div class="notice" markdown="1">
**풀이**

```python


```
</div>

<div class="notice--success" markdown="1">
**14.**   
2개의 문자(ASCII CODE)를 입력받아서 순서를 바꿔 출력해보자.
</div>

<details>
<summary>아스키 코드란</summary>
<div markdown="1">

컴퓨터가 문자를 읽을 수 있도록 문자에 대응하는 숫자들이 존재한다.

ex ) A => 1100001

이때의 문자가 '아스키 문자'이며, 숫자가 '아스키 코드'이다.

</div>
</details>

<div class="notice" markdown="1">
**풀이**

```python


```
</div>

<div class="notice--success" markdown="1">
**15.**   
실수(float) 1개를 입력받아 저장한 후, 저장되어 있는 값을 소수점 셋 째 자리에서 반올림하여 소수점 이하 둘 째 자리까지 출력하시오.
</div>

<details>
<summary>TIP</summary>
<div markdown="1">

반올림 함수 `round()`를 이용하면 된다.

</div>
</details>

<div class="notice" markdown="1">
**풀이**

```python


```
</div>

<div class="notice--success" markdown="1">
**16.**   
int형 정수 1개를 입력받아 공백을 사이에 두고 3번 출력해보자.
</div>

<div class="notice" markdown="1">
**풀이**

```python


```
</div>

<div class="notice--success" markdown="1">
**17.**   
어떤 형식에 맞추어 시간이 입력될 때, 그대로 출력하는 연습을 해보자.<br>
콜론(:) 기호를 기준으로 두 수가 각 변수에 저장된다.<br>
입력 : 3:15<br>
출력 : 3:15
</div>

<details>
<summary>TIP</summary>
<div markdown="1">

`split()`의 매개변수로 문자열을 분할하기 위한 기준을 정의할 수 있다.
문자열의 메소드(함수)인 `format()`을 이용하면 문자열 내부에 변수값을 대입할 수 있다.

</div>
</details>

<div class="notice" markdown="1">
**풀이**

```python


```
</div>

<div class="notice--success" markdown="1">
**18.**   
년, 월, 일을 입력받아 지정된 형식으로 출력하는 연습을 해보자.<br>

**입력**<br>
연, 월, 일이 ".(닷)"으로 구분되어 입력된다.<br>
**출력**<br>
입력받은 연, 월, 일을 yyyy.mm.dd 형식으로 출력한다.<br>
입력 : 2020.2.9<br>
출력 : 2020.02.09<br>
(단, m 혹은 d가 한 자리 수인 경우 앞에 0을 붙여 출력한다.)
</div>

<div class="notice" markdown="1">
**풀이**

```python


```
</div>

<div class="notice--success" markdown="1">
**19.**   
주민번호는 다음과 같이 구성된다.<br>

`XXXXXX-XXXXXXX`<br>

앞의 6자리는 생년월일(yymmdd)이고 뒤 7자리는 성별, 지역, 오류검출코드이다.<br>
주민번호를 입력받아 형태를 바꿔 출력해보자.<br>

**입력**<br>
주민번호 앞 6자리와 뒷 7자리가 '-'로 구분되어 입력된다.<br>
(입력값은 가상의 주민번호이다.)<br>
ex)110011-0000000<br>
**출력**<br>
'-'를 제외한 주민번호 13자리를 모두 붙여 출력한다.<br>

입력 : 000907-1121112<br>
출력 : 0009071121112
</div>

<div class="notice" markdown="1">
**풀이**

```python


```
</div>