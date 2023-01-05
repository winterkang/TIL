# 딕셔너리
- 키(key)-값(value) 쌍으로 이뤄진 모음(collection)
```  
   변수 = { 'key' : 'value' }
   변수['key']
   >> 'value'
```  
  - key : 불변 자료형(immutable)
    - string, integer, float, boolean, tuple, range
  - value : 어떠한 형태든 관계 없음
    - list, dictionary 등
- 변경 가능하며(mutable), 반복 가능함(iterable)
  - 딕셔너리 반복시 키 반환
- 리스트, 튜플, 문자열 → 인덱싱, 슬라이싱으로 요솟값 얻음
- 딕셔너리 → key를 이용해 value를 얻음

</br>

1. 쌍 추가
```
>>> a = {1: 'a'}
>>> a[2] = 'b'
>>> a
{1: 'a', 2: 'b'}
```
2. 요소 삭제
```
>>> del a[1]
>>> a
{2: 'b', 'name': 'pey', 3: [1, 2, 3]}
```
3. key를 통해 value 얻기
```
>>> a = {1:'a', 2:'b'}
>>> a[1]
'a'
>>> a[2]
'b'
```
* 주의 사항
  - key는 고유한 값이므로 key가 중복되면 1개를 제외한 나머지 key는 무시됨
  - key에 리스트를 사용하면 KeyError
  
</br>

## 딕셔너리 관련 함수
1. key 리스트 만들기 (keys)
```
>>> a = {'name': 'pey', 'phone': '010-9999-1234', 'birth': '1118'}
>>> a.keys()
dict_keys(['name', 'phone', 'birth'])
```
* 딕셔너리 for문
```
>>> for k in a.keys():
...    print(k)
...
name
phone
birth
```
* 리스트로 변환
```
>>> list(a.keys())
['name', 'phone', 'birth']
```
2. value 리스트 만들기 (values)
```
>>> a.values()
dict_values(['pey', '010-9999-1234', '1118'])
```
3. key, value 쌍 얻기 (items)
```
>>> a.items()
dict_items([('name', 'pey'), ('phone', '010-9999-1234'), ('birth', '1118')])
```
4. key : value 쌍 모두 지우기 (clear)
```
>>> a.clear()
>>> a
{}
```
5. key로 value 얻기 (get)
```
>>> a = {'name':'pey', 'phone':'010-9999-1234', 'birth': '1118'}
>>> a.get('name')
'pey'

>>> a.get('phone')
'010-9999-1234'
```
* 딕셔너리에 존재하지 않는 키로 값을 가져오려는 경우 : None 또는 KeyError
```
>>> a = {'name':'pey', 'phone':'010-9999-1234', 'birth': '1118'}
>>> print(a.get('nokey'))
None

>>> print(a['nokey'])
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
KeyError: 'nokey'
```
```
>>> a.get('nokey', 'foo')
'foo'
```
6. 해당 key가 딕셔너리 안에 있는지 조사하기 (in)
```
>>> a = {'name':'pey', 'phone':'010-9999-1234', 'birth': '1118'}
>>> 'name' in a
True

>>> 'email' in a
False
```

</br>

# 모듈 / 라이브러리

- 모듈 : 다양한 기능을 하나의 파일로
- [라이브러리](https://docs.python.org/ko/3/library/datetime.html) : 다양한 패키지를 하나의 묶음으로
![모듈/라이브러리](/Python/img/모듈,라이브러리.png)
![sort/sorted](/Python/img/sort,sorted.png)

- 패키지 : 다양한 파일을 하나의 폴더로
- pip : 이것을 관리하는 관리자
