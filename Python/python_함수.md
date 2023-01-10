> Abstraction (추상)
- 복잡한 내용을 숨기고, 기능에 집중하여 사용할 수 있음
- 재사용성, 가독성, 생산성
- 변수와 같은 존재

> Decomposition
- 기능을 분해, 재사용 가능

</br>

# 함수 Function
- 특정한 기능을 하는 코드의 조각(묶음)
- 필요 시 호출해서 간편히 사용
- 함수 기본 구조 : input을 받아서 output을 한다

</br>

> 자주 사용하는 함수

|함수|설명|
|---|---|
|len(s)|길이|
|sum(iterable, start=0)|합계, 문자열X|
|max(iterable)|가장 큰 값|
|min(iterable)|가장 작은 값|

</br>

> 수학 관련 함수

|함수|설명|
|---|---|
|abs(x)|절댓값|
|divmod(a, b)|몫과 나머지|
|pow(base, exp, mod=None)|base의 exp거듭제곱 반환 /  mod가 있는 경우, base의 exp거듭제곱의 모듈로 mod반환|
|round(number, ndigit=None|반올림 / nidigit이 생략되거나 None이면 가까운 정수 반환|

</br>

> 논리 관련 함수

|함수|설명|
|---|---|
|all(iterable)|모든 요소가 참이면 True 반환|
|any(iterable)|하나라도 참이면 True 반환 / 비었으면 Flase|

</br>

> 기타 함수

|함수|설명|
|---|---|
|bin(x)|정수 -> 이진 문자열로|
|hex(x)|정수 -> 16진수 문자열로|
|oct(x)|정수 -> 8진수 문자열로|
|ord(c)|유니코드 문자 -> 유니코드 숫자 반환|
|chr(i)|유니코드 숫자 -> 문자 반환|

</br>

> 응용 함수

|함수|설명|
|---|---|
|map(function, iterable)|반복 가능한 iterable에 function 적용 후 결과를 map 객체로 반환|
```
# 리스트를 정수형으로 바꿔서 합하기
numbers = ['1', '2', '3']
result = 0
for number in numbers:
    result += int(number)
print(result)

>> 6
```
> 다음 두가지 방법은 같은 결과를 가진다
```
# 리스트에 추가하기
numbers = ['1', '2', '3']
new_numbers = []
for number in numbers:
    new_numbers.append(int(number))
print(new_numbers)

>> [1,2,3]
```
```
# map함수를 사용해서 리스트에 추가하기
numbers = ['1', '2', '3']
new_new_numbers = map(int, numbers)
print(new_new_numbers)
print(list(new_new_numbers))

>> [1,2,3]
```
![map](/Python/img/map.png)

</br>

# 사용자 함수 Custom Function

`Defining Function`
```
def function_name():
    #code block
    return returning_vlaue # 값 반환
```
- return문을 한번만 사용하면서 두 개 이상의 값을 반환하려면 튜플 사용!
  - 함수 정의 : def function_name(x, y):
  - 값 반환 : return x - y, x + y
  - 함수 호출 : function_name(4, 5)
  - 튜플로 반환 : (-1, 20)

- 값을 무한하게 받을 경우 (unpacking *)
  - 함수 정의 : def add(*numbers):
  - 타입 : * 튜플 
  - 값 반환 : return total(numbers)
  - 출력 : print(add(1,2,3)) >> 6

`Calling Function`
```
function_name()
```
