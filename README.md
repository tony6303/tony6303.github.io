# welcome tony6303.github.io
## My first blog
* Post 1
* Post 2
***
commit & push test
***

push : 로컬 저장소(내 컴퓨터)의 내용을 원격 저장소(깃허브)로 업로드 합니다.

commit : 세이브지점, 스냅샷 같은 개념, 변경사항이 생길때마다 코멘트와 함께 커밋해주는것이 좋습니다.

pull : 원격 저장소(깃허브)의 내용을 로컬 저장소(내 컴퓨터)로 업로드 합니다.

### **용어1**

stage(추적): 작업공간에서 변경이 발생한 파일을 다음 커밋에 포함되도록 예약하는 것을 추적이라고 합니다. 
어떤 파일을 추적하면 그 파일을 스테이지되었다고 합니다. 

추적되는 파일은 스테이지 영역(stage area)에 들어가 있게 됩니다.

unstage(추적해제): 추적하고 있는 파일을 스테이지 영역에서 제외하는 것을 언스테이지라고 합니다.

### **용어2**

브랜치(branch): 커밋에서 분기하면 브랜치가 됩니다. 말 그대로 한 갈래; 가지를 의미합니다.

여러 명이 하나의 프로젝트에서 깃 없이 작업하는 것이 얼마나 혼란스러울 것인가? 
일반적으로, 작업자들은 메인 프로젝트의 브랜치를 따와서(branch off), 자신이 변경하고 싶은 자신만의 버전을 만든다. 
작업을 끝낸 후, 프로젝트의 메인 디렉토리인 “master”에 브랜치를 다시 “Merge”한다.

새 브랜치를 “cats”로 부르고 싶으면, git branch cats를 타이핑한다.

브랜치에서 작업을 끝내고, 모든 협업자가 볼 수 있는 master 브랜치로 병합할 수 있다. 
git merge cats는 “cats” 브랜치에서 만든 모든 변경사항을 master로 추가한다.

master: 기본 설정된 브랜치에 붙는 이름입니다.

origin: 기본 설정된 원격 주소에 붙는 별명입니다.

태그(Tag): 알아보기 쉽게 하기 위해서 커밋(commit)에 달아 주는 별명입니다.

HEAD: 현시점에서 작업중인 브랜치를 가리키는 포인터입니다. 작업공간이 현재 위치해 있는 브랜치를 가리킵니다.

### **기본(로컬) 명령어**

git status : 마지막 커밋 이후 작업공간에서 변경이 일어난 모든 파일들을 나열하는 명령어입니다. 
현재 추적되고 있는 파일을 초록색으로 표시하고 그렇지 않은 파일은 빨간색으로 나타냅니다.

git add : 해당 파일을 추적(stage)시키는 명령어입니다. 추적되고 있는 파일만 커밋에 포함됩니다. 
주로 git add . 의 형태로 사용합니다. git add . 명령어는 변경이 일어난 모든 파일을 추적하게 합니다.

git rm : 해당 파일을 추적해제(unstage)시키는 명령어입니다. git add 명령어의 반대입니다.

git commit : 커밋을 추가하는 명령어입니다. 커밋 명령어를 사용해서 커밋을 추가하는 것을 가리켜 '커밋한다'라고 부릅니다.
 주로 git commit -m "(코멘트; 커밋에 덧붙일 말)" 형식으로 사용합니다. 
 (참고: 명령어 입력중 덧붙일 말 사이에 줄바꿈을 추가하고 싶을 수 있습니다. 터미널에서는 Shift + Enter 를 입력하면 개행합니다.)

git log : 커밋 이력을 열람할 수 있도록 하는 명령어입니다.

git checkout : 커밋을 불러오는 명령어입니다. git checkout (커밋 해시) 형식으로 사용합니다.
커밋 해시는 전부 적을 필요는 없고 다른 커밋 해시와 중복되지 않아 고유하다면 앞의 몇 자리만 기입해도 인식됩니다.
(팁: 가장 최근의 커밋을 기준으로 하여 작업공간에서 발생한 변경사항을 모두 버리고 
원래 상태로 돌아가는 명령어는 git checkout -- . 입니다.)

git diff : 커밋과 커밋 사이의 변경사항을 확인할 수 있게 하는 명령어입니다.

### **원격 명령어**

git remote : 원격과 로컬 저장소를 연결시키는 명령어입니다.

git clone : 로컬에서의 git init에 해당하는 명령어입니다. 
원격에서 저장소를 최초로 가져올 때는 git pull 대신 git clone을 쓰는 것입니다.

git fetch : 원격에서 업데이트된 저장소를 받아와서 로컬 저장소를 갱신하는 명령어입니다.

git pull : git fetch 한 다음 작업공간까지도 갱신하는 명령어입니다.

git push : 원격에 내 로컬 저장소를 올리는 명령어입니다. 
원격과 로컬 저장소 변경 사이에 충돌이 있는 경우에 덮어씌운다, 합친다, 브랜치 등 선택할 수 있는 
몇 가지 옵션은 있지만 그런 일은 거의 일어나지 않습니다.
