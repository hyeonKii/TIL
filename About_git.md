### GIT
Git은 리눅스 베네딕트 토발즈가 만들었다.

Git과 같은 시스템을 Distributed Version Control System이라고도 한다.

코드 공유, 이력관리, 협업을 위해서 사용한다.

git init

.git 폴더를 생성한다. 이것은 local repository라고 한다.

*.gitignore 파일을 만드는 이유는 원격 저장소에 올리고 싶지 않을 때 이 파일을 만든다.

 

git add <올릴 파일>

add를 하게 되면 stage area에 올라간다.

 

git commit -am / -m <커밋 메세지>

local repo에 올라간다.

 

git remote add origin <원격저장소 url>

로컬과 원격 저장소 간 연결하는 명령어

 

git push -u origin main

원격저장소의 별칭을 보통 origin이라고 하고 그 origin 저장소의 디폴트 브랜치를 main이라고 한다.

따라서, origin의 main 브랜치에 작업한 파일을 올린다는 의미다.

 

git clone <원격 저장소 url>

원격저장소의 소스들을 한번에 받는 명령어다.

 

특정 브랜치를 클론하는 법

git clone -b <브랜치 이름> <원격 저장소 url>

 

git pull

서버의 최신 소스를 다운받는 것

 

git pull origin <브랜치 이름>

특정 브랜치 pull 하기

 

서버와 연결된 저장소 끊는 법

git remote rm origin

 

git reset vs git revert

git reset은 시간여행을 하여 과거로 돌아가면 해당 과거시점 이후에 커밋한 것은 사라진다

*git reset --hard의 경우, 특정 과거시점으로 돌아가면 이후의 작업은 완전히 사라지므로 주의해야 한다.

 

git revert도 시간여행을 하는 것이지만 history를 지우지 않고 남긴다.

 

git branch

Main이라는 나무기둥에 브랜치를 만드는 것이다.

 

git checkout <브랜치 이름>

해당 브랜치로 전환하는 것이다.

 

git branch -r

원격저장소 브랜치 보기

 

git branch -a

원격/로컬 모든 브랜치 보기

 

git branch -d <브랜치 이름>

로컬 브랜치 삭제

 

git push --delete origin <브랜치 이름>

원격 브랜치 삭제

 

원격저장소의 특정 브랜치 가져오기

git checkout -t origin/<브랜치 이름>

 

git rebase

베이스를 재설정한다는 것이다.

커밋의 시간에 관계없이 마지막에 merge 되는 브랜치의 커밋을 가장 뒤에 붙이는 것이다.
git stash

작업 중이 파일들을 임시 저장 장치에 저장해주는 것

이렇게 하므로 stage를 clean한 상태로 만들어 준다.


