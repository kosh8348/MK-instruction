# Git 명령어 정리

## Git 일반 명령어

`git init` : 현재 폴더를 Git으로 관리하겠다.  
`git status` : 현재 프로젝트의 상태 보기  
`git add README.md` : 프로젝트에 파일 추가(준비 상태)  
`git commit -m "README.md"` : 프로젝트에 파일 추가(추가된 상태)  
`git log` : 작업 이력(commit) 확인하기

## Git add, commit 되돌리기

### commit 되지 않은 작업

`git add`진행 이전
    `git restore <파일이름>`

`git add`진행 이후
    `git restore --staged <파일이름>`

### commit 이 진행된 작업

`git log` 로 commit 확인 후 되돌릴 목표 commit 복사  
`git rest OOOOOO` : commit이 되돌아감


## Github 관련 명령어

- `git clone <Git 주소>` : Github의 프로젝트 컴퓨터로 가져오기  
    1. 주소를 가져온다.  
    2. 만들어진 파일을 확인 후 `git add` + `git commit -m` 진행

- `git remote add origin <Git 주소>` : 컴퓨터의 프로젝트 Github에 올리기  
    1. 주소를 가져온다  
    2. `git push --set-upstream origin main` 입력

`git push` : 원격 저장소에 commit 업로드

### Github의 새로운 이력을 컴퓨터로 가져오기

Github에 연결된 프로젝트 폴더에서 `git pull`


## Conflict가 발생했을 때

1. 충돌이 발생한 파일을 수정해준다.
>내용은 각각의 변경 이유를 살피고 직접 작성해야 한다.

2. `git add`와 `git commit`을 이용해 새로운 commit을 생성
3. **CONFLICT**를 해소하는 새로운 commit을, 모두 공유하기 위해 **push**
4. 최종적으로 Github에 해당 내용이 반영되었음을 확인한다.
   