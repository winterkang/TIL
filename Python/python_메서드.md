### 타입.메서드()


> string type

1. 문자열 탐색
   
|문법|설명|
|---|---|
|s.find(x)|x의 첫 번째 위치 반환. 없으면 -1 반환|
|s.index(x)|x의 첫 번째 위치 반환. 없으면 오류 발생|
|s.isalpha()|알파벳 문자 여부(유니코드 상 letter)|
|s.isupper()|대문자 여부|
|s.islower()|소문자 여부|
|s.istitle()|타이틀 형식 여부|

2. 문자열 변경

|문법|설명|
|---|---|
|s.replace(lod, new[,count])|바꿀 대상 글자를 새로운 글자로 바꿔서 반환|
|s.strip([chars])|공백이나 특정 문자를 제거|
|s.split()|공백이나 특정 문자를 기준으로 분리|
|.join([iterable])|구분자로 iterable을 합침|
|s.capitalize()|가장 첫 번째 글자를 대문자로 변경|
|s.title()|띄어쓰기 기준으로 첫글자는 대문자, 나머지는 소문자로 변환|
|s.upper()|모두 대문자로 변경|
|s.lower()|모두 소문자로 변경|
|s.swapcase()|대소문자 서로 변경|

</br>

> list

1. 값 추가 및 삭제

|문법|설명|
|--------|-------|
|l.append(x)|리스트 마지막에 값을 추가|
|l.insert(i,x)|정해진 위치 i에 x값 추가|
|l.remove(x)|리스트 가장 왼쪽에 있는 항목 x제거, 항목이 없을 경우 valueerror|
|l.pop(x)|리스트 가장 오른 쪽에 있는 항목 반환 후 제거|
|l.clear()|모든 항목 삭제|

2. 탐색 및 정렬

|문법|설명|
|------|-------|
|l.reverse()|리스트를 역순으로 뒤집음, 정렬x|
|l.sort()|리스트를 정렬, None반환, 원본 변경됨|
|l.sorted()|정렬된 리스트 반환, 원본 변경X|
|l.count(x)|원하는 값의 개수 반환|


</br>

> set

|문법|설명|
|---|---|
|s.add(x)|세트 s에 없다면 x 추가|
|s.pop(x)|랜덤 반환하고 해당 항목 제거, 세트가 빈 경우 keyerror|
|s.remove(x)|항목 x를 s에서 삭제, 항목이 존재하지 않을 경우 keyerror|

</br>

> dictionary

|문법|설명|
|---|---|
|.get(key)|value 가져옴, 디폴트 값은 none|
|.pop(key)|key가 딕셔너리에 있으면 제거 후 값 반환하고 아니면 디폴트 반환, 디폴트 없으면 keyerror|
|.update(key = value)|값을 제공하는 key, value로 덮어씀|
