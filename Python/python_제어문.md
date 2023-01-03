# 제어문 (Control Statement)
- 위에서 아래로 순차적 명령 수행
- 조건에 따라 반복 제어
- flow chart로 표현 가능

</br>

## 조건문 (Conditional Statement)
- 참/거짓을 판단할 수 있는 조건식과 함께 사용
```
if <expression>:
    # Run this code block
else:
    # Run this code block
```

</br>

> 복수 조건문
```
if <expression>:
    # Code block
elif <expression>:
    # Code block
elif <expression>:
    # Code block
else:
    # Code block
```

</br>

> 중첩 조건문
```
if <expression>:
    # Code block
    if <expression>:
        # Code block
else:
    # Code block
```

</br>

## 반복문(Loop Statement)
- for문
- while문
- 반복제어

</br>

> for문
- for문은 시퀀스(string, tuple, list, range)를 포함한 순회가능한 객체(iterable)요소를 모두 순회
- 처음부터 끝까지 모두 순회하므로 종료조건 필요X
```
for <변수명> in <iterable>:
    # Code block
```
```
예시1. 반복 가능한 객체: 각 요소가 필요할 때
fruits = 'apple'
for fruit in fruits:
    print(fruit)
```
```
>> a
>> p
>> p
>> p
>> l
>> e
```
```
예시2. 반복 가능한 객체: 인덱스가 필요할 때
fruit = 'apple'
for i in range(len(fruit))
    print(i,fruit[i])
```
```
>> 0 a
>> 1 p
>> 2 p
>> 3 l
>> 4 e
```

> 반복문 제어
- break
  - 반복을 종료
  ```
    for i in range(10):
        if i > 1:
            print("0과 1만 필요해!")
            break
        print(i)
  ```
  ```
    >> 0
    >> 1
    >> 0과 1만 필요해!
    >> 2부터 9까지 if문에 들어가면 break
  ```
- continue
  - continue 이후의 코드 블록은 수행하지 않고 다음 반복 수행
  ```
    for i in range(6):
        if i % 2 == 0:
            continue
        print(i)
  ```
  ```
    >> 1
    >> 3
    >> 5
    >> continue를 만나면 print(i)가 실행되지 않고 바로 다음 반복 실행
  ```
- for - else
  - 끝까지 반복문 실행한 이후에 else문 실행
    - break를 통해 중간에 종료되는 경우 else문 실행X
    - else문은 break로 중단되었는지 여부에 따라 실행
  
  </br>

  ```
    for char in 'apple':
        if char == 'b':
            print('b')
            break
    else:
        print('b가 없습니다')
  ```
  ```
  >> b가 없습니다
  ```
    ```
    for char in 'banana':
        if char == 'b':
            print('b!')
            break
    else:
        print('b가 없습니다')
  ```
  ```
  >> b!
  ```

</br>

> enumerate( )
- index와 원소를 동시에 루프를 돌릴 수 있음 (=tuple)
```
for i, letter in enumerate(['A', 'B', 'C']):
    print(i, letter)

>> 0 A
>> 1 B
>> 2 C
```
- index와 원소를 각각 다른 변수에 할당하고 싶다면 unpacking을 해야 함
```
for n in enumerate(['A', 'B', 'C']):
    print(n)

>> (0, 'A')
>> (1, 'B')
>> (2, 'C')
```


[파이썬 작동원리를 알고 싶다면 여기를 누르세요](https://pythontutor.com/)

