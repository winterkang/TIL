# [입력과 출력](https://docs.python.org/ko/3.12/tutorial/inputoutput.html#)
```
with open(파일명, 모드 선택('r','w'..), encoding = 'utf8')as f:
      변수 = f.read()/write()
```

</br>


# JSON
- 웹 어플리케이션에서 데이터를 전송할때 사용
- 딕셔너리와 동일 구조(key-value) , 주석 불가능
- 자바스크립트에서 쓰는 표기법을 이용하는 텍스트 문서

`파이썬 딕셔너리를 json 파일로 저장`
```

import json

d = dict()
d['id'] = 1
d['name'] = 'pie'
d['test'] = ['game', 'tv', 'work']

file_path = '저장할 파일 경로 url'

with open(파일명, 'w', encoding = 'utf8') as f:
    json dump(d, f, indent = 4)
```
`파일 읽어오기`
```

import json

file_path = '읽어올 파일 경로 url'

with open(file_path, 'r', encoding = 'utf8') as f:
    data = json.load(f)

print(data['pie']) # 값에 접근
print(data['pie']['gender']) # 중첩된 값 접근

# dump 함수를 이용해서 콘솔에 json으로 읽은 파일 출력
print(json.dumps(data, indent = 4)) 
```

`json파일을 읽고 수정하고 다시 json파일로 저장`

```


import json

file_path = '읽어올 파일 경로 url'

with open(파일명, 'r')as f:
  data = json.load(f)

-- 수정할 파이썬 딕셔너리 내용 --

with open(file_path, 'w', encoding = 'utf-8') as f:
  json.dump(data, f, indent= 4)
```