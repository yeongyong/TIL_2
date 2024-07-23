# Git과 Github

## [1] Git 이란 ?
- (분산) 버전 관리 프로그램
  
## [2] Git 시작하기
누가 어떠한 변경 사항을 남겼는지 git이 자동으로 만들어 주기 위해 필요함 !
global한 정보를 주었기 때문에, 최초 한 번만 설정하면 됨.

    '''
    git config --global user.name "이름"
    git config --global user.email "메일주소"
    '''
확인하기 위해서는 
    '''
    git config --global--list
    '''

## [3] Git의 3공간
  1. working directory  -> 분장실
  2. staging area       -> 무대
  3. repository         -> 사진 저장소

이 순서로 사진을 찍어 내기 위해서 기본 명령어를 사용!

## [4] Git 기본 명령어 
### (1) git init
    '''
    # 로컬 저장소를 만든다 -> 현재 작업 중인 디렉토리(폴더)를 git으로 관리한다는 의미.
    git init
    '''
이후, '(master)' 표시가 뜨게 된다.
### (2) git add 
working directory에서 작업이 완료된 파일을 staging area 위로 올린다.
    '''
    git add 파일명
    '''
### (3) git commit 
staging area에 있는 사진을 찍음 (기록함).
    '''
    git commit -m "변경 사항이 기록된 이유"
    '''
버전 관리 프로그램 git이 자동으로 변경 사항에 대한 "육하원칙"을 작성하기 위해, 왜 바꿨는지에 대한 정보가 필요해서 메세지를 남김.


### (4) git status
각 파일들의 상태를 알려줌 (Untracted, modified, New file, ...)
    '''
    git status
    '''

### (5) git log
변경 사항들의 기록을 보여줘
    '''
    git log --oneline
    '''

## Github
서버 컴퓨터처럼 원격에서 나의 변경 사항 기록들을 가지고 있또록 사용할 수 있다.

### (1) repository 생성
1. 우측 상단 + 버튼 눌러서 repository 만든다.
2. URL 생성된다 -> 원격 저장소의 주소를 의미한다.
3. 복사 : 

### (2) 로컬 저장소와 연결
    '''
    # 원격 저장소 연결
    git remote add origin URL

    # 원격 저장소 연결을 확인
    git remote -v
    '''
### (3) 변경 사항을 로컬 저장소에서 원격 저장소로 보내기
로컬 저장소의 commit(변경사항)을 원격 저장소에 반영해줌.
'''
git push origin master
'''

