### 1주차에 가장 처음 들은 말 : "개발은 혼자 하는 일이 아니다"

## 개발은 혼자 하는 일이 아니다

개발은 여러사람이 같이 모여서 하는 것이다
그래서 아래와 같은 내용들이 거의 무조건 필요하다.
### 우리가 이메일, usb로 공유할 수는 없으니까!!!

 
 1. 어떤 파일이 수정됐는지,

 2. 누가 수정했는지,

 3. 언제 수정됐는지,

 4. 어떻게 수정됐는지

## 우리는 파일을 만듬으로써 파일에게 생명을 준다.

# Git 최초 설정

--------

밑에 있는 내용들은 GIT의 최초 설정들을 의미한다.
최초 설정 (컴퓨터에서 깃을 처음 사용한다면 입력)

git config --global user.name "<깃허브 이름>"

git config --global user.email “<깃허브 이메일>”

# Git init

"git init"은 폴더를 git을 사용하는 git 저장소로 만든다.
우리는 "git log"를 통해 이 폴더에서의 누가 언제 어디서 무엇을 작업했는지 알 수 있다.

# Git으로 파일 관리하기
1.  디렉토리에 Git 저장소를 만들기
2.  Git으로 관리할 대상 등록하기
3.  파일 수, 후 로컬 저장소로 옮기기



# vs code에 해야하는 일들

vs code에 일단 파일을 연다.
git add "파일명" // staging area로 보낸다.
git add . // 작업폴더의 모든 파일을 전부 스테이징한다.
.




# git hurb에 올리기 

마크다운 문법 작성후

git push origin main
ㄴ파일을 github에 업로드

이러면 git hurb에 올라가서 직접 확인 가능


# 그외의 다양한 마크다운 문법들

## Commit Message - type
chore
* 코드 외의 설정을 바꾼 경우

docs
* 문서화

test
* 테스트 코드


## Commit Message - type

feat
* 새로운 기능을 추가한 경우

refactor
* 기존 코드를 개선한 경우

fix
*버그를 수정한 경우

이렇게 사용된다.

...

...


2024-1-Beginner-Study    C411029 김은호

https://github.com/ChiHo7575/ChiHo7575