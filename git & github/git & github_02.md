# clone vs pull
- clone : 원격저장소 복제, 원격에 있는 프로젝트 시작할때(협업)
- pull : 원격저장소 커밋 가져오기, 프로젝트 개발 중 다른 사람 커밋 받아올떄

</br>

# Branch
- 여러 개발자들이 동시에 다양한 작업을 할 수 있게 만들어 주는 기능
- 독립적인 작업흐름을 만들고 관리함

![branch](/git%20%26%20github/img/branch.png)

</br>

## Branch 명령어
1. 브랜치 생성
```
   $ git branch (branch name)
```
2. 브랜치 이동 
```
    $ git checkout (branch name)
```
3. 브랜치 생성 및 이동 : 위의 두 과정을 한번에 해결
```
    $ git checkout -b (branch name)
```
4. 브랜치명 변경
```   
    $ git branch -m (브랜치명) (새로운 브랜치명)
```
5. 브랜치 목록 확인
```   
    $ git branch
```
6. 브랜치 삭제
```   
    $ git branch -d (branch name)
````

</br> 

# Merge
- 새로 만든 브랜치의 변경 사항을 'master'브랜치에 병합

</br>

(1) fast-forward merge
```
$ git checkout master
 : 'master'브랜치에 새로 만든 브랜치를 넣기 위해서를 'master'브랜치에 'HEAD'가 위치해야함.
$ git merge (병합할 브랜치 이름) 
```
</br>

`
'issue2'와 'issue3' 두 개의 브랜치가 생성되어 동시에 여러 작업을 한다고 가정
`

(2) 동시에 여러 작업 하기

```
1. issue2 브랜치에서 작업한 파일을 add,commit한다.
    $ git add 파일명
    $ git commit -m '메시지'
        → 원격 저장소에 저장됨
2. issue3로 전환한다. 
    $ git checkout issue3
     → issue3에는 issue2에서 작업한 내용이 없으므로 pull 해야 함
    $ git add 파일명
    $ git commit -m 'pull설명'
```

(3) non fast-forward merge
```
issue2와 issue3브랜치에서 변경한 부분 모두 'master'브랜치에 병합한다면?
```
```
$ git checkout master
$ git merge issue2
→ master 브랜치에서 issue2 병합 완료
```
```
$ git merge issue3

→ CONFLICT !!! 

왜? 각각의 브랜치에서 변경한 내용이 같은 행에 포함되어 있기 때문에

그래서? 일일이 수정해야 해결가능
```
```
충돌 부분 수정 후
$ git add 파일명
$ git commit -m 'issue3브랜치병합'
→ On branch master 
```

</br>

# Git Flow
- Git을 활용하여 협업하는 흐름
- branch를 활용하는 전략

![gitflow](/git%20%26%20github/img/git%20flow.png)

## Github Flow 기본원칙
1. master branch는 반드시 배포 가능한 상태일 것 
2. feature branch는 각 기능의 의도를 알 수 있도록 작성할 것
3. commit message는 매우 중요, 명확하게 작성할 것
4. Pull Request를 통해 협업
5. 변경사항을 반영하고 싶다면, master branch에 병합함

</br>

# Fork
1. Github 저장소에서 우측 상단의 Fork버튼을 누른다.
2. 본인 원격저장소에 저장될 이름 작성하고 Creat Fork
3. Fork로 받아온 저장소를 로컬로 clone후 branch생성
``` 
   $ git clone (clone url)
   $ git branch 생성할 브랜치 이름
   $ git checkout 생성한 브랜치 이름
```
4. add, commit, push
   $ git add .
   $ git commit -m '메시지'
   $ git push origin 브랜치 이름
5. github 저장소에서 변경사항 확인하고
6. 'Compare & Pull request' 클릭 후 PR메시지를 작성하고 'Create pull request'클릭