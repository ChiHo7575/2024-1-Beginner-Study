# git log



### commit 기록을 최신 순으로 확인
### 옵션을 사용하면 각 커밋을 한 줄에 요약


# Commit id 

### commit의 식별을 위해 사용하는 40자 길이의 16진수
### 중복 확률은 2의 80제곱 분의 1
### SHA-1 해시 함수를 사용


# Head

Head 는 현재 작업 중인 위치를 가리킨다.
현재 작업중인 브랜치의 가장 최근 commit을 나타낸다
다음 commit의 base가 되는 commit이다.
새로운 commit이 생기면 Head도 변경 가능하다.



# Git status


현재 내가 입력한 세 가지 상태에 따라 파일을 분류하여 확인한다.


# Commit --amend

마지막 commit의 내용에 변경이 있을 때 사용한다.

완전히 새로운 commit으로 대체한다.

Commit id가 바뀐다.

Vim으로 진입하여 commit 메세지를 수정하게 된다.

""git commit --amend -m "커밋 메세지""" (-m option으로 vim 진입 없이 commit 메세지 수정)


""git commit --amend --no-edit"" (--no-edit option으로 commit 메세지 수정없이 commit 수정)




*********주의 사항************  

다른 사람이 작업 기반으로 삼고 있는 commit은 amend하면 안된다.


# reset

commit을 제거하는 데 사용
3가지 옵션 존재한다 (soft, mixed(default), hard)


""git reset '--option' "commit id""" (돌아갈 commit의 id를 사용)




## reset --soft ()

커밋만 취소
변경 사항이 Staging Area로 돌아간다.

## reset --mixed

커밋을 취소
변경 사항을 working directory로 돌아간다.

## reset --hard 

커밋을 취소
변경 사항을 모두 제거하고 이전 커밋으로 돌아간다.




# reset 대 revert

## reset 은 commit을 삭제 하므로 위험하다

## commit을 공유하는 다른 브랜치에도 영향을 줄 수 있다.

## commit을 삭제하기보다 생성하여 되돌리는 revert가 안전하다.

