> 컴퓨터 프로그래밍 언어
  - 컴퓨터(Computer) : Caculation(조작) + Remember(저장)
  - 프로그래밍(Programming) : 명령어의 모음(집합)
  - 언어 : 자신의 생각을 나타내고 전달하기 위해 사용하는 체계. 문법적으로 맞는 말의 집합
```  
  컴퓨터 프로그래밍 언어 : 컴퓨터에게 명령하기 위한 약속!
```
- 선언적 지식(declarative knowledge) : 사실에 대한 내용
- 명령적 지식(imperative knowledge) : How-to

</br>

# Python

## 객체와 변수 
- 객체(Object) : 숫자, 문자, 클래스 등을 값을 가지고 있는 모든 것
- 변수(Variable) 
  - 객체를 참조하기 위해 사용되는 이름
  - 변수는 할당 연산자(=)를 통해 값을 할당(assignment)
  - type ( )
    - 변수에 할당된 값의 타입
   ```
    a = 1
    print(type(a))
    >> <class 'int'>
<!--
  - id ( )
     - 변수에 할당된 값(객체)의 고유한 아이덴티티 값
  - 변수에 할당된 값(객체)의 고유한 아이덴티티 값-->
  - 같은 값을 동시에 할당할 수 있음
  
      ` x = y = 1004`
  - 다른 값을 동시에 할당 할 수 있음(mulitple assignment)
      
      ` x , y = 1 , 2`
  ```
  : 오른쪽의 값을 왼쪽에 할당하는 것!
  ```
## 실습 문제
```
x = 10 y = 20 일 때, 각각 값을 바꿔서 저장하는 코드를 작성하시오
```
- 방법 1) 임시 변수 활용
  
        z = x , x = y, y = z
- 방법 2) pythonic 
  
        y ,x = x, y
        print(x, y)
  
</br>

---

## 식별자(Identifiers)
- 파이썬 객체(변수, 함수, 모듈, 클래스 등)를 식별하는데 사용하는 이름(name)
- 규칙
  - 식별자와 이름은 영문 알파벳, 언더스코어(_), 숫자로 구성
  - 첫 글자에 숫자가 올 수 없음
  - 길이 제한이 없고, 대소문자를 구별
  - 다음의 키워드는 예약어로 사용할 수 없음
  
    ```
    False, None, True, and, as, assert, async, await, break, class, continue, def, del, elif, else, except, finally, for, from, global, if, import, in, is, lambda, nonlocal, not, or, pass, raise, return, try, while, with, yield
    ```

  - 내장함수나 모듈 등의 이름으로도 만들면 안됨
    - 기존의 이름에 다른 값을 할당하게 되므로 더이상 동작하지 않음

    ```
    print(5)
    print = 'hi'
    print(5)
    >> TypeError
    ```

</br>

---
## 자료형 (Data Type)
- 숫자
  - 수치형(Numeric Type)   
    - int(정수, integer)
    - float(부동소수점, floating point number)
    - complex(복소수, complex number)
  - 불린형(Boolean Type)
    - True(1) / False(0) 
    - 비교/논리 연산에 활용
- 시퀀스(Sequence)
  - 문자열(String)
  - 튜플(Tuple)
  - 리스트(List)
  - 레인지(Range)
- 컬렉션(Collection)
  - 집합(Set)
  - 딕셔너리(Dictionary)
- None

</br>

---
## 컨테이너(Container)
- 여러 개의 값을 담을 수 있는 것(객체)
- 순서가 있는데 데이터(ordered) vs 순서가 없는 데이터(unordered)
- 순서가 있다 != 정렬되어 있다
- 시퀀스
  - 문자열(immuatable) : 문자들의 나열
  - 튜플(muatable) : 변경 가능한 값들의 나열
  - 리스트(immuatable) : 변경 불가능한 값들의 나열
  - 레인지(immuatable) : 숫자의 나열
- 컬렉션/비시퀀스
  - 집합(muatable) : 유일한 값들의 모음
  - 딕셔너리(immuatable) : 키-값들의 모음

</br>

---
## 연산자(Operator)
> 산술 연산자(Arithmetic operator)

|연산자|내용|
|------|---|
|+|덧셈|
|-|뺄셈|
|*|곱셈|
|%|나머지|
|/|나눗셈|
|//|몫|
|**|거듭제곱|

> 복합 연산자(In-place Operator)

|연산자|내용|
|------|---|
|a = a + b|a += b|

> 비교 연산자(Comparison Operator)

  |연산자|내용|
  |------|---|
  |<|미만|
  |<=|이하|
  |>|초과|
  |>=|이상|
  |==|같음|
  |!=|같지않음|

> 논리 연산자(Logicak Operator)

  |연산자|내용|
  |------|---|
  |A and B|모두 참이거나 거짓|
  |A or B|둘 중 하나만 참이라도 참, 그렇지 않으면 거짓|
  |Not|참 거짓의 반대의 결과|

> 시퀀스형 연산자(Sequence Operator)
   
  ` 컴퓨터는 0부터 숫자를 센다!`
  - 인덱싱(Indexing)
    - a[0] → 첫번째
    - a[-1] → 뒤에서 첫번째
  - 슬라이싱(Slicing)
    - a[2:5] → 2부터 4까지
  
  
> 이스케이프 연산자(Escape sequence)

  |이스케이프|내용|
  |--|---|
  |\n|개행|
  |\t|탭|

  

</br>

---
## 문자열(String Type) : 문자열의 나열
  - 타입 : string
  - 표기법 : 작은 따옴표(''), 큰 따옴표("") 활용
  - 문자열은 <u>변경 불가능</u>하고 나열할 수 있다.
  - 결합
```
     'a' + 'b' >> ab 
```
  - 반복
```
     'a' * 3 >> aaa 
```
  - 포함
```
     'a' in 'apple' >> True
```

</br>

---
## 리스트(List) : 변경 가능한 값들의 나열
- 순서를 가지며, 서로 다른 타입의 요소를 가질 수 있음
- <u>변경 가능하며</u>(mutable), 반복 가능함(iterable)
- 항상 대괄호 형태로 정의하며, 요소를 콤마로 구분
```
    예시) fruits = ["apple","grape","melon"]
```
- 문자열 길이 
```  
    len(fruits)
  >> 3 
```
- 인덱싱 
```  
    fruits[0] >> apple
    fruits[-1] >> melon
```
- 변경 
```
    fruits[0] = "orange" 
  >> ["orange","grape","melon"]
```
- 추가 : .append( )
```
    fruits.append("orange")
  >> ["apple","grape","melon","orange"]
```
- 삭제 : .pop( )
```
    fruits.pop(2)
  >> ["apple","grape"]
```

<!--- 튜플 : 변경 불가능한 값들의 나열
  - 레인지 : 숫자들의 나열 -->

  
<!--- 컬렉션/비시퀀스
  - 세트 : 유일한 값들의 모음
  - 딕셔너리 : 키-값들의 모음-->
