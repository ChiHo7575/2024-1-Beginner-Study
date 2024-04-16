
# 브랜치 전략
## git flow
## github flow




# 브랜치 관리의 필요성

## 서로의 작업에 영향을 주지 않기 위해 브랜치의 분리 필요
## 각 브랜치가 어떤 작업을 위해 존재하는지 구분 필요
## main 브랜치의 안전한 관리 필요

# 브랜치 보호 규칙

## 승인 없이 Pull Request를 병합할 수 없도록 제한 가능
## 특정 브랜치에 push 가능자를 제한 가능
### -> 브랜치를 안전하게 관리




# 브랜치의 종류
## Main Branches                   Supporting branches
### main(master)                    feature
### develop                         release
###                                 hotfix



# main


## 프로젝트 생성 시 기본으로 생성되는 브랜치
## 영원히 존재하는 첫 번째 브랜치
## 병합될 때마다 제품의 새로운 버전이 탄생
## main이라는 이름 대신 master를 사용하기도 함




# Develop

## 영원히 존재하는 두 번째 브랜치
## feature 브랜치의 기반이 됨


## develop 브랜치에서 분기하여 작업
## 기능 개발 완료 후 다시 develop으로 병합
## 대부분의 이름 가능
###     단, main, master, develop, release, hitfix 제외



# Release 

## 배포 준비를 위한 브랜치
## 자잘한 버그를 수정하고 QA 작업을 함
## develop 브랜치에서 분기하여 main 브랜치로 병합


# Hotfix

## 배포 환경에서 즉각적인 수정이 필요한 경우 사용
## main 브랜치에서 분기
## main, deveop 모두에 병합 필요






# Git Flow 시대는 끝이 났다? 

배포가 수시로 이루어지는 현 시대의 웹앱과는 부적합

Vincent Driessen도  GitHub Flow와 같은 전략을 추천

## GitHub Flow

수시로 배포되는 상황이 Git Flow와 안 어울리는 것을 개선하기 위해 고안한 방법 



