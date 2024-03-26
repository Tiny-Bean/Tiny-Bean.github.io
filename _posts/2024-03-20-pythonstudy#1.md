---
layout: single
title:  "파이썬 스터디 1주차(파이썬의 기초)"
categories:
   - python
---

## 파이썬 스터디 1주차

ICT 멘토링 프로그램에 멘티로 참여하게 됐다.

네 명의 멘티 중 나를 포함한 세 명이 같은 학교에 재학 중이라

본격적인 프로젝트 시작에 앞서 함께 스터디를 진행하기로 했다!

  
우선 데이터 분석과 AI개발에 널리 쓰이는 파이썬 기초를 다지기 위해

"python으로 시작하는 빅데이터 분석 및 인공지능" 이라는 책을 교재로 선정했다.

약 2년 전, 고급파이썬프로그래밍 수업에서 사용했던 교재다. 

당시에 교재의 일부만 사용했고 기억이 많이 날아갔기 때문에

한 번 훑고 넘어가면 좋을 것 같다.

  
이번 주는 *part1: 파이썬의 기초* 의 *chapter05* 까지 공부하고

각자 맡은 부분을 포스팅 해 발표하기로 했다.

내가 맡은 부분은 *2.2 변수의 연산* 과 *chapter04: 함수* 전체다. 

` ** 이왕 공부하면서 포스팅하는 거... 맡은 부분 외에도 공부한 것들은 기록해보려고 한다. ** `

---

## Part1: 파이썬의 기초
### chapter02: 변수와 입.출력 함수

#### 2-1. 데이터형과 변수

##### 1) 데이터형(자료형): 컴퓨터에서 다뤄지는 다양한 **데이터 값들의 유형**을 의미함.

|정수형(int)|실수형(float)|문자열형(str)|부울형(bool)

- 사칙연산 
    - +. -, *, /(나눗셈, 실수형으로 결과 출력), //(나눗셈의 몫 출력), %(나눗셈의 나머지 출력)
- 문자열은 단어나 문장을 저장하기 위해 준비된 데이터형임. C언어에는 문자 1개를 저장하는 문자형(Char)이 있는데, 파이썬에서는 문자형을 문자열형으로 사용하기 때문에 char이 없음.


##### 2) 변수: 데이터를 저장할 수 있는 메모리 공간의 이름.

- 지속적으로 내용을 다른 값으로 갱신할 수 있음.
- 파이썬에서는 변수에 데이터를 할당하는 순간 자동으로 선언됨.
- 등호(=) 연산자를 이용해서 변수값을 저장
- = : 오른쪽 값을 왼쪽에 대입

##### 3) 데이터형을 확인하는 함수: type(), isinstance()

```python
num = 3.5
type(num)
```

출력 결과: <class 'float'>

```python
a = 3
isinstance(a, int)
```

출력 결과: True

##### 4) 부울형 변수(bool)

- True or False의 2가지 논리값 중 하나의 값만 가짐.

```python
exist = True
type(exist)
```

출력 결과: <class 'bool'>




#### 2-2. 변수의 연산

|산술연산자 | 관계연산자 | 논리연산자 | 비트연산자

##### 1) 산술 연산자

```python
a = 3 #정수형
b = 3.5 #실수형
a - b #뺴기
a * b #곱하기
a / b # 나눗셈, 실수형 출력
a // b # 몫 출력
a % b # 나머지 출력
```

##### 2) 관계 연산자

- 두 개의 값이나 변수 간의 관계를 연산함.
- 관계 연산자의 결과는 True / False
- 반드시 연산자의 왼쪽을 주어로 해석해야 함.


코드 예시를 통해 6개의 관계연산자에 대해 알아보자!

```python
a = 3
b = 5
a > b #1. a는 b보다 크다
a < b #2. a는 b보다 작다
a >= b #3. a는 b보다 크거나 같다
a <= b #4. a는 b보다 작거나 같다
a == b #5. a는 b와 같다
a != b #6. a는 b와 같지 않다
```

> **출력 결과**

  a = 3
  b = 5
  a > b #1. a는 b보다 크다
  a < b #2. a는 b보다 작다
  a >= b #3. a는 b보다 크거나 같다
  a <= b #4. a는 b보다 작거나 같다
  a == b #5. a는 b와 같다
  a != b #6. a는 b와 같지 않다


##### 3) 논리 연산자

- 2개의 값이나 변수 간에 논리적인 연산을 수행함
- 논리 연산자의 결과는 True / False

> - end: 그리고
  - or: 또는
  - not: 부정(아니다)

  논리연산자 진리표
  ![image](https://www.google.com/imgres?imgurl=https%3A%2F%2Fwww.dotnetnote.com%2Fdocs%2Fcommon%2F11-03-table-truth-table.png&tbnid=2pW7HS7VVkIYHM&vet=12ahUKEwiaqbyxtJGFAxUjc_UHHVdECU0QMygDegQIARBY..i&imgrefurl=https%3A%2F%2Fwww.dotnetnote.com%2Fdocs%2Fcsharp%2Frelational-logical-operator%2F&docid=z3xy2CnskuAHqM&w=640&h=291&q=%EB%85%BC%EB%A6%AC%EC%97%B0%EC%82%B0%EC%9E%90%20%EC%A7%84%EB%A6%AC%ED%91%9C%20%ED%8C%8C%EC%9D%B4%EC%8D%AC&hl=ko&ved=2ahUKEwiaqbyxtJGFAxUjc_UHHVdECU0QMygDegQIARBY)


논리 연산자의 코드 예시도 살펴보자.
```python
a = 3
b = 5
(a > b) and (a != b) # a는 b보다 크고 a는 b와 같지 않다.
```

> **출력 결과**
  a = 3
  b = 5
  (a > b) and (a != b)

  + (a > b)는 false 이고 (a != b)는 True,   and 연산자는 둘 다 True 인 경우에만 True 값을 출력하므로 결과는 False.


##### 4) 비트 연산자

- 비트 단위로 논리적인 연산이나 자리 이동을 시키는 시프트 기능이 있음.
- 논리연산자의 논리와 동일하지만 비트 단위이기 때문에 1을 True로, 0을 False로 생각하면 됨.
- 정수를 2진수로 변환한 후 연산을 수행함. ~~ 교재 20P 내용인데, 2진수 연산을 비트연산자로 하는 방법은 잘 모르겠다.~~

> **5개의 비트 연산자**
 + & : 비트 단위 and
 + | : 비트 단위 or
 + ^ : 비트 단위 XOR (배타적 논리합, 두 명제의 진리값이 다를 때 True)
 + ~ : 비트 단위 not
 + << : 비트 단위 왼쪽 시프트
 + >> : 비트 단위 오른쪽 시프트


비트연산자 진리표
![image](https://www.google.com/imgres?imgurl=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FQUoY2%2FbtrpPEGsyIE%2FHtdQHrgG9hiZYH3k6uAOC0%2Fimg.png&tbnid=D9wHeFF4b1s3hM&vet=12ahUKEwjPjd6BupGFAxU0k68BHeR8AmUQMygFegQIARBe..i&imgrefurl=https%3A%2F%2Fblog.hexabrain.net%2F92&docid=IWacXSd3wPFbvM&w=683&h=260&q=%EB%B9%84%ED%8A%B8%EC%97%B0%EC%82%B0%EC%9E%90%20%EC%A7%84%EB%A6%AC%ED%91%9C%20%ED%8C%8C%EC%9D%B4%EC%8D%AC&hl=ko&ved=2ahUKEwjPjd6BupGFAxU0k68BHeR8AmUQMygFegQIARBe)


---

### chapter04: 함수

#### 4-1. 사용자 정의 함수

##### 1)

#### 4-2. 함수의 응용
