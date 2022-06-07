## 사용방법
1. git에서 repository 생성
2. 로컬 PC에서 연결할 폴더 위치 복사 (cmd + opt + C)
```bash
$ cd 연결할 폴더 위치
$ git init
$ git add -A
$ git commit -m "first commit"
$ git branch -M main
$ git remote add origin https://github.com/coarzip/myproject.git
$ git push -u origin main 
```

#### vscode에서 작업 후 커밋 방법
1. 소스제어에서 커밋할 내용을 스테이징(+)
2. 커밋(체크표시) 버튼 클릭 후 코멘트 입력
3. 터미널에서 **해당 폴더로 이동 후!!** 
4. push 명령
```bash
$ git push -u origin main
```

#### git의 repository 로컬로 연결하기
1. git에서 repository 생성
2. 로컬 PC 터미널에서 연결할 폴더 위치로 이동
3. clone 명령
```bash
$ git clone [git code  주소]
```
4. 로컬 PC에 해당 폴더가 생성되었는지 확인


#### git merge 방법
git fetch --> get last version
git merge [branch name]
git status  --> conflict or staging
    deleted by them : git rm [file name]
    both modified : 
        nano [file name] : file check
        git add [file name]
git commit -> :q


<br>

-----
## 문제해결

> error: failed to push some refs to 'https://github.com/kaipynuts/TIL.git'

해결 : git에서 token을 만들어 비밀번호 대신 사용
참고자료 : [GitHub Docs](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token) | [블로그1](https://shinye0213.tistory.com/105) | [블로그2](https://hyeo-noo.tistory.com/184)


> git: fatal ... is outside repository at ...

해결 : 상위 폴더를 한글에서 영문으로 변경하여 사용
참고자료 : [블로그](https://gyong0117.tistory.com/entry/M1-%EB%A7%A5%EB%B6%81-Git-fatal-is-outside-repository-at-%EC%98%A4%EB%A5%98-%ED%95%B4%EA%B2%B0)