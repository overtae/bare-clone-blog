---
title: "[JavaScript] 값 vs. 식 vs. 문"
date: 2022-07-17
categories:
  - JavaScript
tags:
  - 값
  - value
  - 식
  - expression
  - 문
  - statement
excerpt: 값, 식 그리고 문에 대해 알아보자
---

## 값 Value

값은 **식이 평가되어 생성된 결과**라고 할 수 있고, 변수에 할당된다.

**💡 평가?** 식을 해석해서 값을 생성하거나 참조하는 것
{: .notice}

변수에 할당되는 것은 값이므로 a라는 변수에 `1 + 2`를 할당한다면 a에 3이 할당된다.

이 말은 곧 아래 코드와 같다.

{% highlight jsx linenos %}
var a = 1 + 2; // a = 3
{% endhighlight %}

위와 같은 방법으로 값을 식으로 생성할 수도 있지만 리터럴을 사용하는 가장 기본적인 방법도 존재한다.

## 리터럴 Literal

리터럴은 사람이 이해할 수 있는 문자 또는 약속된 기호를 사용해 값을 생성하는 표기법을 의미한다.

- 숫자 리터럴 `1`은 숫자 `1`을 의미
- 문자열 리터럴 `'hello'`는 문자열 `'hello'`를 의미

리터럴을 사용할 경우 *정수, 부동소수점, 2진수, 8진수, null, 객체, 배열 등*의 다양한 종류의 값을 생성할 수 있다.

## 표현식 Expression

표현식(식)은 값으로 평가될 수 있는 모든 문(statement)을 의미한다.

이 말은 곧, 표현식이 평가되면 새로운 값을 생성하거나 기존의 값을 참조한다는 것이다.

표현식은 리터럴, 식별자, 연산자, 함수 호출 등의 조합으로 이뤄질 수 있다.

{% highlight jsx linenos %}
var a = 1 + 2;
// 식별자 표현식 x > 3으로 평가 됨
x + 3; // 6
// 표현식은 다른 표현식의 일부가 되어 새로운 값을 만들어낼 수 있다.
{% endhighlight %}

## 문 Statement

문은 프로그램을 구성하는 기본 단위이자 **최소 실행 단위**이다. 문의 집합으로 이루어진 것이 바로 프로그램이며, 문을 작성하고 순서에 맞게 나열하는 것이 프로그래밍이다.

여러 <span style="color:#3b9cba">**토큰**</span>으로 구성되며, 여기서 토큰이란 **문법적인 의미를 가지며 문법적으로 더 이상 나눌 수 없는 코드의 기본 요소**를 의미한다.

예를 들어 *키워드, 식별자, 연산자, 리터럴, 세미콜론, 마침표 등*이 있겠다.

문은 명령문이라고도 부른다. 이 말은 즉, **문이 실행되면 명령이 실행되고 무슨 일인가가 일어나게 된다**는 것이다.

문은 *선언문, 할당문, 조건문, 반복문 등*으로 구분 가능하다.

## 표현식인 문 vs. 표현식이 아닌 문

표현식은 문의 일부일 수도 있고 그 자체로 문이 될 수도 있다.

{% highlight jsx linenos %}
// 변수 선언문은 값으로 평가 불가 > 표현식 X
var x;
// 1, 2, 1 + 2, x = 1 + 2 모두 표현식
// 아래 구문은 표현식이면서 완전한 문이기도 하다.
x = 1 + 2;
{% endhighlight %}

표현식인 문과 표현식이 아닌 문을 구별하는 가장 간단한 방법은 **변수에 할당해 보는 것**이다.

{% highlight jsx linenos %}
var a = function () {} // 할당 가능 > 함수 선언문은 표현식 O
var b = var a // 할당 불가 > 변수 선언문은 표현식 X
var c = if (x > 1) { console.log(x); } // 할당 불가 > 조건문은 표현식 X
var d = for (;;) {} // 할당 불가 > 반복문은 표현식 X
{% endhighlight %}

표현식인 문은 값처럼 사용할 수 있다.

{% highlight jsx linenos %}
// 표현식인 문은 값처럼 사용할 수 있다
x = 100; // 평가(evaluate)할 경우 100이 된다.
var foo = x = 100;
console.log(foo); // 100
{% endhighlight %}

## ASI Automatic Semicolon Insertion

코드 블록은 언제나 문의 종료를 의미하는 **자체 종결성**을 갖기 때문에 중괄호로 묶은 코드 블록 뒤에는 세미콜론을 붙이지 않는다.

문의 끝에 붙이는 세미콜론은 생략 가능한데, 자바스크립트 엔진이 소스코드를 해석할 때 문의 끝이라고 예측되는 지점에 자동으로 세미콜론을 붙여주는 **세미콜론 자동 삽입 기능**이 암묵적으로 수행되기 때문이다.

ASI의 동작 결과와 개발자의 예측이 일치하지 않는 경우가 가끔 있기도 해 **세미콜론 사용을 권장**하는 분위기라고 한다.

정확히 말하자면 개발자가 ASI의 동작을 제대로 예측하지 못해 아래와 같이 제대로 활용하지 못하는 경우가 있는 것이다.

{% highlight jsx linenos %}
function foo () {
  return
    {}
  // ASI의 동작 결과 => return; {};
  // 개발자의 예측 => return {};
}

console.log(foo()); // undefined

var bar = function () {}
(function() {})();
// ASI의 동작 결과 => var bar = function () {}(function() {})();
// 개발자의 예측 => var bar = function () {}; (function() {})();
// TypeError: (intermediate value)(...) is not a function
{% endhighlight %}

**Notice:** 이 게시물은 [모던자바스크립트 Deep Dive 교재](https://book.naver.com/bookdb/book_detail.nhn?bid=16710547)와 [딥다이브 스터디](https://www.youtube.com/watch?v=3ZP3VPlrr0U)를 참고하였습니다.
{: .notice--info}