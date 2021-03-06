# Quest 00. Hello, git


## Introduction
* git은 2018년 현재 개발 생태계에서 가장 각광받고 있는 버전 관리 시스템입니다. 이번 퀘스트를 통해 git의 기초적인 사용법을 알아볼 예정입니다.

## Topics
* git
  * `git clone`
  * `git add`
  * `git commit`
  * `git push`
  * `git pull`
  * `git branch`
  * `git stash`
* GitHub

## Resources
* [git, 분산 버전 관리 시스템](http://www.yes24.com/24/goods/3676100?scode=032&OzSrank=1), 인사이트
* [GitHub 사용 설명서](http://www.yes24.com/24/Goods/17638082?Acode=101), 교학사
* https://try.github.io
* http://pcottle.github.io/learnGitBranching

## Checklist
* 버전 관리 시스템은 왜 필요한가요?
    
    * 개별 파일 혹은 프로젝트 전체를 이전 상태로 되돌리거나 시간에 따른 변경사항을 검토할 수 있다.
    * 문제가 되는 부분의 수정했는지, 누가 언제 이슈를 만들어냈는지 등을 알 수 있다.
    * 파일을 잃어버리거나 무언가 잘못되어도 쉽게 복구할 수 있다.
    * 이 모든 장점을 누리는 데 큰 노력이 들지 않는다.  
  
 
* git 외의 버전관리 시스템에는 무엇이 있나요? git은 그 시스템과 어떤 점이 다르며, 어떤 장점을 가지고 있나요?
  
  * 버전 관리 시스템은 다음과 같이 구분할 수 있다. 
    * 로컬 버전 관리 시스템(Local VCS)
      pc 내에 데이터베이스를 저장하여 관리, 협업이 힘들고 바이러스나 기기 고장 시 복구 불가능. (RCS, SCCS 등)
    * 중앙집중식 버전 관리 시스템(CVCS) 
      별도의 서버를 두고 데이터베이스를 관리하며 클라이언트가 중앙 서버에서 수정을 원하는 파일을 받아서 사용, 협업이 가능하고 누가 무엇을 하는지 쉽게 알 수 있는 등 관리가 용이하나 협업의 규모가 클 때 수정 충돌이 발생할 우려가 있으며 중앙 서버에 문제가 생기면 복구가 불가능(CVS, SVN 등)
    * 분산 버전 관리 시스템(DVCS) 
      * git이 여기에 해당
      * 서버에 파일을 저장하는 것은 동일하지만 개별 사용자가 파일 전체를 자신의 로컬에 복제하여 사용, 또한 수많은 리모트 저장소를 두어 동시에 다양하게 협업할 수 있으며 기존 서버 뿐만 아니라 로컬, 리모트 저장소를 가지기 때문에 문제가 발생시 나머지 저장소를 통해 복구가 가능.
* git의 `clone`/`add`/`commit`/`push`/`pull`/`branch`/`stash` 명령은 무엇이며 어떨 때 이용하나요? 그리고 어떻게 사용하나요?
  * `git clone` - 서버 프로젝트를 로컬에 내려받는 명령어
    * `git clone[저장소 주소]`
  * `git add` - 작업한 내용을 git이 추적할 수 있는 staging area로 보내는 명령어
    * `git add .` - working directry 전체
    * `git add [파일명]` - 해당 파일만
  * `git commit` - staging area로 보내진 내용을 로컬에 저장하는 명령어
    * `git commit -m "메시지"`
  * `git push` - 리모트 저장소에 commit을 저장하는 명령어
    * `git push [원격 저장소명][원격 브랜치명]`
  * `git pull` - 리모트 저장소의 내용을 로컬로 보내는 명령어
    * `git pull [원격 저장소명][원격 브랜치명]`
  * `git branch` - master(줄기)에서 빠져나온 개별 작업 공간(가지)을 만드는 명령어
    * `git branch` - branch 확인
    * `git branch [브랜치명]` - 새 branch 생성
    * `git branch checkout[브랜치명]` - branch 전환
  * `git stash` - 아직 마무리하지 않은 작업을 잠시 저장해두고 branch를 넘어가는 명령어
    * `git stash` - 작업을 임시로 저장
    * `git stash list` - stash 목록 확인
    * `git stash apply` - 했던 작업을 다시 가져오기
    * `git stash apply --index`- 위와 어떻게 다른 건지 아직 정확히 이해가 안감.  

## Quest
* github에 가입한 뒤, [이 커리큘럼의 github 저장소](https://github.com/KnowRe/WebDevCurriculum)의 우상단의 Fork 버튼을 눌러 자신의 저장소에 복사해 둡니다.
* [GitHub Desktop](https://desktop.github.com/)을 다운받아 설치합니다.
* Windows의 경우 같이 설치된 git shell을, MacOSX의 경우 터미널을 실행시켜 커맨드라인에 들어간 뒤, 명령어를 이용하여 복사한 저장소를 clone합니다.
  * 앞으로의 git 작업은 되도록 커맨드라인을 통해 하는 것을 권장합니다.
* 이 문서가 있는 폴더 바로 밑에 있는 sandbox 폴더에 파일을 추가한 후 커밋해 보기도 하고, 파일을 삭제해 보기도 하고, 수정해 보기도 하면서 각각의 단계에서 커밋했을 때 어떤 것들이 저장되는지를 확인합니다.
* `clone`/`add`/`commit`/`push`/`pull`/`branch`/`stash` 명령을 충분히 익혔다고 생각되면, 자신의 저장소에 이력을 push합니다.
