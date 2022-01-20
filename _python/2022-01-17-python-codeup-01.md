---
title: "[파이썬 기초 100제] 1강 출력"
date: 2022-01-17
categories:
  - Python
tags:
  - python
  - 기초 100제
  - 코드업
---

<div class="notice--success" markdown="1">
**1.**  
Hello 출력하기
</div>

<div class="notice" markdown="1">
**풀이**

```python
print('Hello')
```
</div>

<div class="notice--success" markdown="1">
**2.**  
Hello World 출력하기
</div>

<div class="notice" markdown="1">
**풀이**

```python
print('Hello World')
```
</div>

<div class="notice--success" markdown="1">
**3.**  
Hello World 출력하기<br>
(두 줄에 걸쳐 줄을 바꿔 출력하기)
</div>

<div class="notice" markdown="1">
**풀이**

```python
# 방법 1
print('Hello\nWorld')
# 방법 2
print('''\
Hello
World
''')
# 방법 3
print("""\
Hello
World
""")
```
</div>

<details>
<summary>TIP</summary>
<div markdown="1">

따옴표를 `'''`(작은따옴표) 혹은 `"""`(큰따옴표) 와 같이 3개씩 사용하면 입력하는 모양대로 출력된다.<br>
처음 따음표 `'''` 뒤에 역슬래시`\`를 해주어야 직관적으로 코딩할 수 있게 된다.<br>
만약 역슬래시를 안해주면 한 줄의 공백 후에 출력이 된다.

```python
print('''
AA
BB
''')

# 출력
(한 줄 공백)
AA
BB
```

</div>
</details>

<div class="notice--success" markdown="1">
**4.**  
'Hello' 출력하기<br>
(단, 작은 따옴표도 함께 출력한다.)
</div>

<div class="notice" markdown="1">
**풀이**

```python
print("'Hello World'")
# 큰따옴표 안에 작은 따옴표를 넣어주면 된다.
```
</div>

<div class="notice--success" markdown="1">
**5.**  
"Hello World" 출력하기<br>
(단, 큰따옴표도 함께 출력한다.)
</div>

<div class="notice" markdown="1">
**풀이**

```python
print('"Hello World"')
```
</div>

<div class="notice--success" markdown="1">
**6.**  
"!@#$%^&*()" 출력하기<br>
(단, 큰따옴표도 함께 출력한다.)
</div>

<div class="notice" markdown="1">
**풀이**

```python
print('"!@#$%^&*()"')
```
</div>

<div class="notice--success" markdown="1">
**7.**  
"C:\Download\hello.cpp" 출력하기<br>
(단, 큰따옴표도 함께 출력한다.)
</div>

<div class="notice" markdown="1">
**풀이**

```python
print('"C:\Download\hello.cpp"')
```
</div>

<div class="notice--success" markdown="1">
**8.**  
`┌┬┐`<br>
`├┼┤`<br>
`└┴┘` 출력하기
</div>

<div class="notice" markdown="1">
**풀이**

```python
print('''\
┌┬┐
├┼┤ 
└┴┘
''')
# 큰따옴표나 작은 따옴표 3개를 이용하면 된다.
```
</div>

**Notice:** 이 게시물은 [우리밋_woorimIT](https://www.youtube.com/watch?v=7sykajCtgCw&list=PLSK4WsJ8JS4dOszA7Zr8paqI81Mv27tNq&index=2)님의 유튜브를 참고하였습니다.
{: .notice--info}