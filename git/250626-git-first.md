# Git

## git 이란?
분산형 버전관리 시스템(distributed Version Control System)

## git 특징
- 비선형적 개발(수천개의 브랜치) 가능
- 분산형 저장소 지원

## Git 주요 개념
1. Working directory 
2. staging area 
3. local repository 
4. remote repository


1 -> 2 : git add 
2 -> 3 : git commit
3 -> 4 : git push
3 <-> 1 : git switch
4 -> 3 : git pull

## Git _ configuration Set up
$ git config --global user.name “{username}”
$ git config --global user.email “{emailaddr}”
$ git config --global core.editor “vim”
$ git config --global core.pager “cat”

* cat .gitconfig파일에 editor=vim 과 같이 따음표가 없어야 함.

## Git 확인

$ git clone {github_repo_ur0l:username/repo-addr}
$ cd {repo-addr}
$ git status

## Git 사용하기

$ vi README.md
$ git status
#변경 사항 확인
$ git add README.md
#Staging으로 넣기
$ git commit
#로컬 레포지토리에 저장
$ git push origin main
#리모트 레포지토리에 저장

#Access Token 사용법
설정 > 개발자 셋팅 > classic 토큰 만들기> 토큰 복사하기
> 처음 접속시 토큰 인증 필요.(git clone url)하면 인증창이 뜸.

## 주요 기능

### add

### commit
commit할 때 vi창이 열림, 최상단에 변경에 대한 내용(제목) 작성 필수

#### conventional commits
- 설명하는 문장형이 아닌 구나 절의 형태로 작성
- Capitalize
- prefix 꼭 달기
-- feat: 기능 개발 관련
-- fix: 오류 개선 혹은 버그 패치
-- docs: 문서화 작업
-- test: test 관련
-- conf: 환경설정 관련
-- build: 빌드 작업 관련
-- ci: Continuous Integration 관련
-- chore: 패키지 매니저, 스크립트 등
-- style: 코드 포매팅 관련

### Branch
- Branch list
(local) $ git branch
(remote) $ git branch -r
(all) $ git branch -a
- Create new branch
$ git branch {branch name}
- switch to branch
$ git switch {branch name}

### Merge

### push

### 번외_ .gitignore
- 특정 파일이나 디렉토리를 추적하지 않도록 명시하기 위한 파일

