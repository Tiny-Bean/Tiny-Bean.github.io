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

**이왕 공부하면서 포스팅하는 거... 맡은 부분 외에도 공부한 것들은 기록해보려고 한다.** 

---

# Part1: 파이썬의 기초
## chapter02: 변수와 입.출력 함수

### 2-1. 데이터형과 변수

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




### 2-2. 변수의 연산

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

  False
  True
  False
  True
  False
  True
  

##### 3) 논리 연산자

- 2개의 값이나 변수 간에 논리적인 연산을 수행함
- 논리 연산자의 결과는 True / False

> 논리연산자
  - end: 그리고
  - or: 또는
  - not: 부정(아니다)

  논리연산자 진리표
  ![image](https://www.dotnetnote.com/docs/common/11-03-table-truth-table.png)


논리 연산자의 코드 예시도 살펴보자.
```python
a = 3
b = 5
(a > b) and (a != b) # a는 b보다 크고 a는 b와 같지 않다.
```

> **출력 결과**
  
  False

  + (a > b)는 false 이고 (a != b)는 True,   and 연산자는 둘 다 True 인 경우에만 True 값을 출력하므로 결과는 False.


##### 4) 비트 연산자

- 비트 단위로 논리적인 연산이나 자리 이동을 시키는 시프트 기능이 있음.
- 논리연산자의 논리와 동일하지만 비트 단위이기 때문에 1을 True로, 0을 False로 생각하면 됨.
- 정수를 2진수로 변환한 후 연산을 수행함. ~~교재 20P 내용인데, 2진수 연산을 비트연산자로 하는 방법은 잘 모르겠다.~~

---

**+추가**
다시 보니 이진수 비트 연산도 그냥 논리연산자 진리표대로 계산하면 된다^^...

> **5개의 비트 연산자**
 + & : 비트 단위 and
 + \| : 비트 단위 or
 + ^ : 비트 단위 XOR (배타적 논리합, 두 명제의 진리값이 다를 때 True)
 + ~ : 비트 단위 not
 + << : 비트 단위 왼쪽 시프트
 + \>\> : 비트 단위 오른쪽 시프트


비트연산자 진리표
![image](https://blog.kakaocdn.net/dn/QUoY2/btrpPEGsyIE/HtdQHrgG9hiZYH3k6uAOC0/img.png)


---

## chapter04: 함수

### 4-1. 사용자 정의 함수

모듈에서 지원하지 않는 기능이 필요하다면, 즉 나만의 함수가 필요하다면?  

사용자 정의 함수를 사용!

> ##### 함수의 기본 형식
 def 함수명(입력인자):
     명령문 1   
     (명령문 2  
     ...)    
     (return ...)   


> ##### 함수의 유형 

|   유형     |     입력값     |   출력값(반환값)   |
| :-------: | :----------: | :-------------: |
|     1     |      X       |        X        |
|     2     |      X       |        O        |
|     3     |      O       |        X        |
|     4     |      O       |        O        |


##### <입력값이 있는 경우>

함수의 입력값이 있다면 다음에 오는 괄호 란에 입력 인자를 나열하면 된다. (없으면 비워두기)   


코드 예시를 통해 살펴보자.

```python
def double(num):
    print(num, '의 제곱:', num*num)
double(3) #3이 함수의 입력값
```

이 경우 double 함수는 어떤 값을 화면에 출력할 뿐, 함수가 어떤 값을 반환하는 것은 아니다. (반환값이 없기 때문!)  

##### <반환값이 있는 경우>   

**함수의 반환은 반환값(함수가 계산한 값의 결과)를 함수를 호출한 곳으로 다시 돌려준다.**

보통 함수의 마지막 부분에 위치, 다음과 같이 "return" 명령어를 사용한다.

> **return([복수개]반환값 또는 변수)**


##### <입력값이 없고 반환값도 없는 경우>    

```python
def hello():
    print('Hello!')
hello() #함수를 호출한 것뿐, return 값은 없음
```

이 경우 "Hello!"가 출력되었다고 함수의 출력값(반환값)이 있는 게 아니다.

함수릐 출력이란 **return**명령어가 있는 반환이 존재해야 한다!!


##### <입력값과 출력값이 모두 있는 경우>    

```python
def double(num):
    return num*num #함수를 호출한 곳으로 반환값(num*num)을 돌려줌
result = double(3) 
print('%d의 제곱:%d' % (3, result))
```

이 경우 double 함수의 입력값은 3이고, return 명령문에 의해 함수를 호출한 곳으로 3의 제곱 값이 반환된다. 빈환된 값은 변수 result에 저장되어 "3의 제곱: 9"가 출력된다. 


##### <단수 반환과 복수 반환>

대부분의 다른 프로그래밍 언어와 달리 파이썬에서는 복수 개의 반환이 가능하다.

코드 예시를 통해 살펴보자!


우선, **단수 반환**은 호출한 함수가 반환하는 값이 1개라는 의미이다.

```python
def double(n):
    square = n * n
    return square #함수를 호출한 곳으로 반환값(num*num)을 돌려줌
print(double(7)) #double 함수의 입력값은 7
```

print 함수 내부에서 double 함수를 호출했다.

입력된 7의 값은 변수 n에 저장되고 7의 제곱값이 square에 저장된다. 

return 명령문에 의해, square 값이 함수를 호출한 print 함수 쪽으로 반환되어 49가 출력된다.


```python
def add(a,b):
    sum = a+ b
    return sum #함수를 호출한 곳으로 반환값(sum)을 돌려줌
print(add(3,5)) #입력값은 3과 5
```

위의 add()함수는 입력값이 2개다.

3은 변수 a에, 5는 변수 b에 저장되며 둘을 더한 값인 8이 sum에 저장된다.

return 명령문에 의해, 함수를 호출한 print 함수 쪽으로 sum 값이 반환되어 8이 출력된다.

---

다음으로, **복수 반환**에 대해서 알아보자.

반환되는 값이 2개 이상일 때는 콤마로 나열하면 된다.

```python
def add_sub(a,b):
    sum = a + b
    diff = a - b
    return sum, diff # 반환값 두 개를 콤마로 나열
print(add_sub(3,5)) #입력값은 3과 5
```

출력 결과는 (8, -2) 이다.


>**Quiz 4.1**   
 (1) sum(n) 함수를 호출하면 1에서부터 n까지의 합을 구하는 sum() 함수를 완성하라.

 
```python
def sum(n):
    sum = 0
    for i in range(1, n+1):
        sum += i
    return sum
print(sum(10))
```

다음 코드를 실행하면 55가 출력된다!


(2) 펙토리얼 값을 계산하는 함수를 완성하라. 

```python
def factorial(n):
    result = 1
    for i in range(n):
        result *= (i+1) # 입력값이 3인 경우 for문의 i는 0,1,2이므로 idp 1을 더해 곱함
    return result
print('3!=', factorial(3))
```

> ##### Tip
- factorial()과 같은 함수들은 수학적으로 많이 사용되므로 math 모듈에서 제공함.
 ```python
 import math
 print('3!=', math.factorial(3))
 ```  


#### 4-2. 함수의 응용

터틀 그래픽으로 파이썬 기초를 복습해보자!

```python
import turtle
turtle.forward(100) #100픽셀만큼 그리기
turtle.right(90) #오른쪽으로 90도 회전
turtle.forward(100) 
turtle.setpos(0,0) # setpos()함수를 이용해서 원점으로 돌아가기
```

>Quiz 4.2
 ```python
 import turtle
 turtle.forward(100) #100픽셀만큼 그리기
 turtle.right(45) #오른쪽으로 45도 회전
 turtle.circle(100) #반지름이 100픽셀인 원 그리기
 turtle.right(45)
 turtle.forward(100)
 turtle.right(90+45) #오른쪽으로 90도 회전 후 45도 회전 -> 원점
 turtle. forward(100)
 ```

```python
 import turtle
 turtle.pencolor(red) # 펜 컬러 지정 / 빨, 노 , 연, 파, 보 지원
 turtle.forward(200)
 turtle.pencolor(blue)
 turtle.circle(100) 
 ```

```python
 import turtle
 turtle.color(red) # 색상 지정 가능 / 기본은 블랙
 turtle.begin_fill() # 폐쇄된 도형 채우기 (위의 지정된 색깔로)
 turtle.circle(50) 
 turtle.end_fill() # 더 이상 채우지 않기
 turtle.circle(100)
 ```


```python
 import random
 print(random.randint(50,100)) # 50~100 에서 무작위로 추출, 각 값도 포함하는 것에 주의!
 ```
 특정한 값을 무작위로 생성하려면 random모듈을 이용하면 된다.    
 randiant()함수를 이용하면 지정한 범위 내의 값을 무작위로 추출하여 값을 반환해준다. 

> Quiz 4.3
 - (1) 50에서 100 사이의 무작위 값을 원의 반지름으로 하는 원을 그리시오.
 ```python
  import turtle
  import random
  rad = random.randint(50, 100)
 turtle.circle(rad)
  ```
  - (2) 노랑, 빨강, 파랑 중 하나의 색상을 무작위로 선택하여 원을 그리는 프로그램을 완성해라.
  ```python
  import turtle
  import random
  col = random.randint(0,1,2)
  if (0 == col):
    turtle.pencolor('yellow')
  elif ( 1 == col):
    turtle.pencolor('blue')
  elif ( 2 == col):
    turtle.pencolor('red')
  turtle.circle(50)
  ```

---

1주차 분량은 여기까지다!

맡은 부분 외에도 다 포스팅 해보려 했으나...

아직은 포스팅에 시간이 꽤 걸려서 나머지는 손으로 교재를 읽고 코드를 쓰며 공부했다.

문단 사이 간격을 더 넓히고 싶은데 아직 방법을 찾지 못했다 ㅋㅋ ㅠ


파이썬도, 블로그도 차근차근 해보겠습니닷

아자아자 팟팅 

 
