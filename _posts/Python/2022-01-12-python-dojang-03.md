---
permalink: /python/python-04/
title: "[파이썬 코딩 도장] Unit 14 문제 풀이"
date: 2022-01-12
categories:
  - Python
tags:
  - python
  - 코딩 도장
excerpt: else 사용하기
---

<div class="notice--success" markdown="1">
**14.6 연습 문제 :**

A 기업의 입사 시험은 필기 시험 점수가 80점 이상이면서 코딩 시험을 통과해야 합격이라고 정했습니다.<br>
(코딩 시험 통과 여부는 True, False로 구분)<br>
다음 소스 코드를 완성하여 '합격', '불합격'이 출력되게 만드세요.

```python
written_test = 75
coding_test = True

___written_test________coding_test________:
    print('합격')
else:
    print('불합격')
# 결과 : 불합격
```

</div>

<div class="notice" markdown="1">
**풀이**

```python
if written_test >= 80 and coding_test:
```

`if written_test >= 80 and coding_test == True`의 방법도 있다.

</div>

<div class="notice--success" markdown="1">
**14.7 심사 문제 :**

표준 입력으로 국어, 영어, 수학, 과학 점수가 입력됩니다.<br>
여기서 네 과목의 평균 점수가 80점 이상일 때 합격이라고 정했습니다.<br>
평균 점수에 따라 '합격', '불합격'을 출력하는 프로그램을 만드세요.<br>
(input에서 안내 문자열은 출력하지 않아야 합니다)<br>
단, 점수는 0점부터 100점까지만 입력받을 수 있으며<br>
범위를 벗어났다면 '잘못된 점수'를 출력하고 합격, 불합격 여부는 출력하지 않아야 합니다.

```python
______________
______________
______________
______________
______________
______________
______________
______________

# 입력 : 89 72 93 82
# 결과 : 합격
```

</div>

<div class="notice" markdown="1">
**풀이**

```python
a, b, c, d = map(int, input().split())
if 0 <= a <= 100 and 0 <= b <= 100 and 0 <= c <= 100 and 0 <= d <= 100:
    if (a + b + c + d) / 4 >= 80:
        print('합격')
    else:
        print('불합격')
else:
    print('잘못된 점수')
```

or을 사용해 모든 점수가 0점 미만, 100점 초과인지 검사하는 방법도 있지만 위의 코드보다 더 길었다.<br>
프로그램을 만들 때 입력 값의 범위를 항상 확인하는 것이 정말 중요하다고 한다.

</div>

**Notice:** 이 게시물은 파이썬 코딩 도장 사이트를 참고하였습니다.
[https://dojang.io/course/view.php?id=7](https://dojang.io/course/view.php?id=7)
{: .notice--info}
