## <p style="text-align:center;">개발 입문 스터디 Quiz 1</p>

#### Example
GDSC는 무엇의 약자인지 적으시오.

- 답: Google Developer Student Clubs

### Q1
Git에서 파일의 상태는 크게 untracked와 tracked로 나눌 수 있다.  
그렇다면 tracked에는 어떤 상태가 있는지 모두 적으시오.

- 답: Git에서 tracked 상태에는 다음과 같은 파일 상태가 있습니다:

Unmodified (수정되지 않음): 파일의 내용이 최근 커밋과 동일하여 변경되지 않은 상태입니다.

Modified (수정됨): 파일의 내용이 변경되어 수정되었지만 아직 스테이징 영역에 추가되지 않은 상태입니다.

Staged (스테이징됨): 수정된 파일이 스테이징 영역에 추가되어 커밋할 준비가 된 상태입니다.

이러한 상태들은 git status 명령어를 사용하여 확인할 수 있습니다.

### Q2
Git에는 세 가지 영역이 있다.  
세 가지 영역을 모두 나열하시오.

- 답: Working Directory (작업 디렉토리): 실제로 파일이 저장되어 있는 디렉토리로, 여기에서 파일을 수정하고 작업합니다.

Staging Area (스테이징 영역 또는 Index): 커밋에 포함될 변경 사항을 임시로 저장하는 공간입니다. 변경된 파일 중 일부만을 스테이징하여 커밋에 포함시킬 수 있습니다.

Repository (저장소): Git이 프로젝트의 메타 데이터와 함께 실제 파일의 스냅샷을 저장하는 곳입니다. 여기에는 프로젝트의 모든 이력과 버전 정보가 포함됩니다.

### Q3
현재 우리는 ```main```브랜치에 있다.  
```develop```이라는 브랜치를 새로 만들고 이동까지 한번에 할 수 있는 명령어를 적으시오.

- 답: git checkout -b develop


### Q4
Working Directory에 있는 파일들을 모두 Staging Area에 추가할 수 있는 명령어를 적으시오.

- 답: git add .


### Q5
```
1. Create a merge commit
2. Squash and merge
3. Rebase and merge
```
위의 세 가지가 어떤 차이가 있는지 간단히 적으시오.

- 답: Create a merge commit (병합 커밋 생성):

두 브랜치의 변경 사항을 합치고, 이를 새로운 병합 커밋으로 기록합니다.
각 브랜치의 이력이 그대로 남아있기 때문에, 브랜치 간의 관계가 명확하게 유지됩니다.
병합 커밋은 두 부모 커밋을 가리키며, 병합 작업에 대한 설명을 포함합니다.

Squash and merge (스쿼시 및 병합):

여러 개의 커밋을 하나로 압축하여 새로운 하나의 커밋으로 만듭니다. 이후 이 압축된 커밋을 기반으로 병합을 수행합니다.
주로 많은 작은 변경 사항을 가진 브랜치를 하나의 의미 있는 커밋으로 합치는 데 사용됩니다.
이 방법을 사용하면 이력이 깔끔하게 유지되지만, 원래 커밋에 대한 정보가 손실될 수 있습니다.

Rebase and merge (리베이스 및 병합):

브랜치를 대상 브랜치로 이동시키고, 대상 브랜치의 최신 커밋 위에 브랜치의 변경 사항을 재적용합니다.
이력의 선형성을 유지하며, 불필요한 병합 커밋이 생성되지 않습니다.
이 방법을 사용하면 병합 커밋을 생성하지 않기 때문에 이력이 깔끔하게 유지되며, 커밋 히스토리가 단순해집니다.

### Q6
```git log --oneline```으로 commit의 기록을 확인해보니  
첫 줄에 ```a1s2d3f (HEAD -> develop) docs: readme 추가```라는 log가 찍혔다.
알 수 있는 사실을 모두 적으시오.

- 답: 커밋 해시(Commit Hash): a1s2d3f
브랜치: HEAD -> develop
커밋 메시지: docs: readme 추가
이 정보를 바탕으로 a1s2d3f 커밋은 develop 브랜치의 최신 커밋이며, 이 커밋은 "docs: readme 추가"라는 커밋 메시지를 가지고 있습니다.

### Q7
```git log --oneline```으로 commit의 기록을 확인해보니 아래와 같은 log를 확인 할 수 있었다.  
```
a1s2d3f (HEAD -> develop) fifth commit
s2d3f4g fourth commit
345hj26 third commit
7g8dg7f second commit
5g568vk first commit
```
이때, fourth commit까지 제거하고 fourth commit과 fifth commit의 변경 사항은
Staging Area에 남아 있길 바란다면 reset을 어떤 옵션과 함께 사용하면 되는지 적으시오.

- 답: git reset --soft 345hj26

위 명령어는 HEAD를 345hj26 커밋으로 이동시키면서, 변경 사항을 Staging Area에 그대로 유지합니다. 따라서 fourth commit과 fifth commit의 변경 사항은 Staging Area에 남게 됩니다.




### Q8
```git log --oneline```으로 commit의 기록을 확인해보니 아래와 같은 log를 확인 할 수 있었다.
```
a1s2d3f (HEAD -> develop) fifth commit
s2d3f4g fourth commit
345hj26 third commit
7g8dg7f second commit
5g568vk first commit
```
reset은 너무 위험하니 revert를 사용하려고 하여 ```fifth commit```을 되돌리고 싶다면 
어떤 명령어를 사용하면 되는지 적으시오. 

- 답: git revert a1s2d3f


### Q9
여러 사람이 협업하는 프로젝트에서 커밋을 되돌려야 한다.  
reset과 revert 중에 어떤 것을 선택할 것인지를 그 이유와 함께 적으시오.

- 답: reset은 이후의 작업에 영향을 미칠 수 있으며, 다른 개발자들의 작업을 망가뜨릴 수 있습니다. 반면에 revert는 특정 커밋을 되돌리는 새로운 커밋을 생성하므로, 이전 이력을 유지하면서도 특정 변경 사항을 취소할 수 있습니다. 그래서 'revert'를 사용하는 것이 좋습니다.
