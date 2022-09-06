---
title: "[파이썬 플라스크] Marshmallow로 Python에서 직럴화/역직렬화 처리하기"
date: 2022-09-04
categories:
  - Python Flask
tags:
  - python
  - flask
excerpt: "데이터 변환"
---

## 직렬화? 역직렬화?

직렬화와 역직렬화란 무엇일까?

> 직렬화 Serialization

메모리를 디스크에 저장하거나 객체를 네트워크 통신이 가능한 (연속된) 형태로 변환하는 것

> 역직렬화 Deserialization

디스크에 저장된 데이터를 읽거나 네트워크 통신으로 받은 데이터를 원래 객체의 형태로 복원하는 것

객체를 Byte나 CSV, XML, JSON 등으로 변환할 수도 있지만 구조적인 데이터의 경우 JSON 형태로의 변환을 권장한다고 한다.

## Python에서의 직렬화/역직렬화

그렇다면 파이썬에서의 직렬화는 어떻게 하는 걸까.

[marshmallow](https://marshmallow.readthedocs.io/en/stable/)는 JSON과 같은 데이터를 파이썬의 객체로 변환해주는 라이브러리이다.

공식 문서를 살펴보면 marshmallow schema는 아래와 같이 쓰일 수 있다 한다.

- 입력 데이터의 **유효성 검사**
- 입력 데이터를 앱 수준 개체로 **역직렬화**
- 앱 수준 개체를 원시 Python 유형으로 **직렬화** — HTTP API에서 사용하기 위해 JSON과 같은 표준 포맷으로 렌더링 가능

## marshmallow Schema 클래스

marshmallow Schema 클래스의 파라미터 중 몇 개만 알아봐보자. — [참고](https://marshmallow.readthedocs.io/en/stable/api_reference.html#marshmallow.Schema)

### dump_only: types.StrSequenceOrSet = ()

: 역직렬화 중에 건너뛸 필드(읽기 전용 필드)

### load_only: types.StrSequenceOrSet = ()

: 직렬화 중에 건너뛸 필드(쓰기 전용 필드)

### many: bool = False

: 객체가 collection일 경우 True로 설정해야 list로 직렬화 된다.


