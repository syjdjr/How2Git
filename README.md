
# 과제 2 보고서 ( 20201857 손유진 ) 

[Github repository](https://github.com/syjdjr/this-.git)

------


# Github 사용법 

Github를 이용하기 위해 우선, 아래와 같이 Github site에 들어간다. 

<img width="960" alt="github" src="https://user-images.githubusercontent.com/81100851/116904208-6118cb80-ac78-11eb-9658-2f05e9916226.png">

Github에 로그인한다. 

<img width="283" alt="sign in github" src="https://user-images.githubusercontent.com/81100851/116904219-6249f880-ac78-11eb-861b-c56a5585b682.png">


다음과 같은 화면에서, 초록색 버튼 new 를 클릭하여 new repository를 만든다. 

<img width="960" alt="new repository" src="https://user-images.githubusercontent.com/81100851/116904214-61b16200-ac78-11eb-8c90-e42f2acb8d65.png">
<img width="943" alt="create new repository" src="https://user-images.githubusercontent.com/81100851/116904204-5fe79e80-ac78-11eb-8da4-cba53ea1cdd3.png">

이는 새로운 저장소를 만듦으로서 코드를 저장할 공간을 마련하는 것이다. 


<img width="953" alt="repository real 주소" src="https://user-images.githubusercontent.com/81100851/116904216-61b16200-ac78-11eb-80a7-ad33af8a8160.png">

<img width="960" alt="repository 주소" src="https://user-images.githubusercontent.com/81100851/116904218-6249f880-ac78-11eb-9521-c24e9594dd77.png">


먼저, 
비어있는 새 파일에 대해 git bash 를 이용하여 다음의 git 명령어들을 사용할 것이다. 


-------------




# init

> 구현 형태: **$ git init** 

현재 git 저장소가 없는 상태이기 때문에  

git 저장소를 생성하기 위해 git init 명령어를 사용한다. 


<img width="437" alt="git init1" src="https://user-images.githubusercontent.com/81100851/117362277-0391b280-aef6-11eb-9939-cfb9c2ea6008.png">

추가적으로, 존재하는 저장소를 비어있는 저장소가 되도록 초기화하는 역할도 한다. 

**요약 및 정리**

*명령어 init은 빈 git 저장소를 생성하는 역할을 함을 알 수 있다.*


# status

> 구현 형태: **$ git status** 

현재 파일에 새로운 파일(markdown.md)을 형성한 상태이다.

원하는대로 새 파일이 git 저장소에 잘 형성되었는지 파악하기 위해 

git status 명령어를 사용한다. 

<img width="437" alt="git status1" src="https://user-images.githubusercontent.com/81100851/117363680-de05a880-aef7-11eb-8c8d-9ae1e74ff52e.png">

명령어 status를 이용하여 파일이 untraced file로 분류되어 git이 아직 관리하고 있지 않고, commit 되지 않았음을 알 수 있었다. 

앞으로의 작업 과정을 확인하면서, 

중간 확인을 위해 status 명령어를 자주 사용함을 알 수 있을 것이다. 

**요약 및 정리**

*status 명령어는 현재 git 저장소의 상태를 알려주는 역할을 한다.*


---


# remote

> 구현 형태: **$ git remote 옵션**  

현재 git 저장소를 만들어 둔 상태이며, git은 github와 협업을 하고 있지 않다. 

git과 github가 협업하도록 

즉, 앞서 만들어 놓은 Github 저장소를 원격저장소로서 사용되게 할 것이기 때문에 remote 명령어를 사용한다. 

<img width="441" alt="git remote1" src="https://user-images.githubusercontent.com/81100851/117364856-63d62380-aef9-11eb-87e0-4d3b77dfe96d.png">

단, Github 원격 서버 저장소의 URL을 origin 이름으로 추가하도록 할 것이다.  



위 이미지와 같이, remote는 여러 가지 옵션을 사용할 수 있다. 

| 옵션 |설명|
|---|--|
|git remote add 이름 저장소_주소 |새로운 원격 저장소를 등록한다.|
|git remote rm 이름 |등록된 원격 저장소를 삭제한다.|
|git remote show 이름 | 지정한 원격 저장소의 정보를 출력한다.|
|git remote prune 이름|더 이상 사용하지 않는 원격 저장소의 추적 브랜치를 삭제한다.| 
|git remote update 이름|git fetch 이름을 실행할 때와 마찬가지로 원격 저장소의 소스를 가져온다.|

옵션 중, 저자의 입장에서 git remote add를 자주 사용하게 될 것이라 예상한다. 

git remote add로 원격 저장소를 등록하면, 다른 명령어를 이용하여 github에서 코드 소스를 이동시키기 편리하기 때문이다. 

**요약 및 정리**

*명령어 remote는 git과 github가 협업하여 문서의 변경사항들을 다룰 수 있도록 문서의 원격 저장소 repository를 추가하도록 해준다.*

---


다음은 파일을 스테이지에 올리는것부터 Github 원격 저장소에 올리는 것까지의 작업들을 시행하는 것이다. 

<img width="437" alt="git add commit push " src="https://user-images.githubusercontent.com/81100851/117365273-07273880-aefa-11eb-9eb0-953469714a8c.png">

첫 번째, 작업 디렉터리에 있는 markdown.md 파일을 스테이지 영역으로 올려 커밋한 후, 스테이지 영역에 있는 것을 원격 저장소로 올린다. 

<img width="443" alt="git add commit push2" src="https://user-images.githubusercontent.com/81100851/117366020-22467800-aefb-11eb-8603-b70e749df6e2.png">

두 번째, 작업 디렉터리에 있는 수정된 markdown.md 파일을 스테이지 영역으로 올려 커밋한 후, 스테이지 영역에 있는 것을 원격 저장소로 올린다. 

<img width="440" alt="git add commit push3" src="https://user-images.githubusercontent.com/81100851/117366027-25416880-aefb-11eb-9f13-3ed36a75e503.png">

세 번째, 작업 디렉터리에 있는 수정된 markdown.md 파일을 스테이지 영역으로 올려 커밋한 후, 스테이지 영역에 있는 것을 원격 저장소로 올린다.

<img width="439" alt="git add commit push4" src="https://user-images.githubusercontent.com/81100851/117366040-283c5900-aefb-11eb-8d0d-928ba3f748ce.png">

네 번째, 작업 디렉터리에 있는 수정된 markdown.md 파일을 스테이지 영역으로 올려 커밋한 후, 스테이지 영역에 있는 것을 원격 저장소로 올린다. 


**단계 : add-commit-push**의 순으로 다른 영역에 파일을 추가하도록 한다는 것을 간단히 기억하고 

자세한 명령어 대한 설명은 아래이다. 

.
.
.
.


# add

> 구현 형태: **$ git add 파일이름** 


위의 4개의 이미지를 살펴보면 git add 명령어가 여러번 사용된 것을 알 수 있다. 

현재 스테이지 영역은 비어있는 상태이다.

스테이지 영역에 markdown.md 파일을 추가하기 위해 add 명령어를 사용한다. 


add 명령어는 디렉토리에 추가된 파일을 스테이지 영역에 추가할 때 사용된다. 
이때, 명령어를 이용해 추가한 후 commit을 해주어 파일을 처리해주어야함을 기억해야한다.

스테이지 영역은 commit 준비가 되 파일들을 저장소에 저장하기 전에 대기하는 장소이기 때문이다. 

다음은 add 명령어의 옵션이다. 

|옵션|설명|
|--|--|
|-f|중복 파일이 있음에도 파일을 추가한다.|
|-p|수정 부분만 추가한다.|
|-v|실행 과정과 결과를 출력한다.|

add 명령어는 모든 수정 파일을 추가하게 하는 **$ git add .**형태를 많이 사용할 것이며, 옵션 중에서는 파일의 수정된 부분을 집중적으로 다루는 -p 를 자주 사용하게 될 것으로 예상된다. 

---


# commit 

> 구현 형태: **$ git commit 옵션** 

위의 4개의 이미지를 살펴보면 git add 명령어가 사용된 이후 git commit 명령어가 사용된 것을 알 수 있다. 

add를 통해 파일이 스테이징 영역에 추가된 상태이므로 파일의 수정 메세지 "this is Github"와 더불어 md파일을 commit 하기 위해 commit 명령어를 사용한다. 



즉, git 명령어 commit은 스테이징 영역에 있는 파일들을 메세지와 함께 commit하는 역할을 한다.



다음은 commit 명령어의 옵션이다. 

|옵션|설명|
|--|--|
|-a|모든 파일을 commit한다.|
|-F 메세지파일| commit 메세지가 담긴 파일을 commit한다.|
|-m 커밋 메세지|commit 메세지를 담는다.|

저자의 입장에서 옵션 -m 을 자주 사용할 것 같다. 단순히 commit 만 수행하는 것이 아니라, 파일의 커밋 메시지를 더불어 추가하기 때문에 개발자는 더욱 문서를 구분하기 편리할 것이다. 

---

# push 

> 구현 형태: **$ git push 로컬저장소 원격저장소**

위의 4개의 이미지를 보면 add 명령어와 commit 명령어 이후에 push 명령어가 사용된 것을 확인할 수 있다. 

현재 md 파일이 commit된 상태에서 원격저장소의 master branch에 최신 파일의 코드를 올리기 위해 명령어 push를 사용한다. 


아래와 같이, 로컬 저장소는 origin, 원격 저장소는 master 로 하여 & git push origin master로 구현하였다. 



이때, origin에 github repository 저장소 주소를 등록해놓았으므로, origin에 등록된 서버(github)로 소스 코드가 등록될 수 있다고 할 수 있다. 

이 과정에서 commit 후 명령어 push를 사용해야 한다는 점을 기억해야한다. 

**요약 및 정리**
*push 명령어를 통해 로컬(local) 즉, 내 컴퓨터에 수정한 코드들이 앞서 설정한 원격저장소 Github에 등록되도록 하므로써 다른 개발자들과 자신의 코드를 공유하는 것을 가능케한다.*

다음은 push 명령어의 옵션이다. 

|옵션|설명|
|--|--|
|-all|모든 수정된 로컬 브랜치를 원격 저장소에 등록한다.|
|-tags|모든 로컬 태그의 변경 사항을 원격 저장소에 등록한다.|

저자의 입장에서 push 명령어의 옵션 중 -all 이 많이 사용될 것이라고 예상된다. 모든 수정된 로컬 브랜치를 원격저장소에 등록할 수 있게 하기 때문에 각각의 사항들을 등록하는 번거로움을 줄여주기 때문이다. 

---


# config

> 구현 방법: **$ git config** 

현재 git은 환경 설정이 되어 있지 않은 상태이다. 

앞으로 branch를 설정하고 통합할 계획이기 때문에 동일한 환경 설정을 통해 conflict를 발생하게 하지 않기 위해 git config 명령어를 사용하여 프로젝트의 git 환경을 설정하도록 한다. 

<img width="437" alt="git config1" src="https://user-images.githubusercontent.com/81100851/117418103-015f4080-af56-11eb-9324-87d9654a8baf.png">

이때 단일 프로젝트가 아니라 전제적인 git 환경을 동일하게 설정하기 위해 git config 명령어의 옵션 --global 을 사용한다. 

**요약 및 정리**

*config 명령어는 전체적인 git을 설정하거나 설정 내용을 확인할 때 사용한다.*


다음은 git config 명령어의 옵션이다.

|옵션|설명|
|--|--|
|--global|git 서버의 전체적인 설정 값을 정할 수 있도록 한다.|
|--list|현재 설정 내용을 한눈에 확인 할 수 있도록 한다.|


(1)--global은 번거롭게 하나씩 설정할 필요 없어 학생(작업자)들이 자주 사용할 수 있다. 

(2)--list 전체 설정 값을 확인할 수 있어 학생(작업자)들이 자주 사용할 수 있다. 

---


# branch 

> 구현 형태: **$ git branch 옵션**

현재 문서는 4번의 수정 과정을 거쳐 4개의 커밋된 markdown.md 파일을 만들었다. 

이 상태에서 앞으로의 수정 작업을 분기하기 위해 branch 명령어를 사용하여 다른 branch를 만들어 줄 것이다.

<img width="437" alt="git branch checkout" src="https://user-images.githubusercontent.com/81100851/117418645-9cf0b100-af56-11eb-87e7-23d12d4aef7c.png">

현재 작업자(현재 저자)는 위 과정을 통해 exp 라는 이름을 가진 branch를 생성하였다. 


branch 명령어를 사용한다는 것은 수정을 거듭한 이후 필요한 문서가 본래 오리지널 문서에 반영 되어야 할 경우, 분기된 서로다른 파일의 내용을 합쳐 새로운 파일을 만들어 낼 수 있다는 의미이다. 

**요약 및 정리**

*branch 명령어는 branch의 생성, 삭제, 이름 변경등 branch를 총 관리를 가능하게 한다.*

다음은 branch 명령어의 옵션이다. 

|옵션|설명|
|--|--|
|-a|브랜치 목록을 모두 출력한다.|
|-r|원격 저장소의 브랜치 목록을 출력한다.|
|-contains commit| 지정된 commit이 포함된 브랜치를 출력한다.|
|-v|현재 branch를 확인하도록한다.|

작업자는  -v 옵션을 자주 사용할 것으로 예상한다. 

branch 명령어를 사용하여 새로운 branch를 만든 이후에, 

작업자가 위치한 현재 branch를 간략히 알 수 있도록 해주기 때문이다.


---


# checkout

> 구현 방법: **$ git checkout** 

branch 명령어를 통해 exp branch가 만들어진 상태이고, 현재 작업자는 master branch에 위치한다. 

앞으로 exp branch에 새 파일을 만들 예정이기 때문에 

checkout 명령어를 통해 master branch에서 exp branch로 이동할 것이다. 

<img width="437" alt="git branch checkout" src="https://user-images.githubusercontent.com/81100851/117418645-9cf0b100-af56-11eb-87e7-23d12d4aef7c.png">

  
  
  
위 작업과 같이 checkout 명령어는 (1) 다른 branch에 위치하도록 이동시키는 역할을 하는 것 뿐만 아니라,

(2) 문서의 수정 변경 사항들을 모두 없애고 이전 파일 상태로 돌아가도록 하기 위해 명령어 checkout을 사용한다. 즉, 마지막 저장시점을 기준으로 변경 이전의 상황으로 되돌아가 파일을 복원시키는 의미이다. 

**요약 및 정리**

*checkout 명령어는 다른 branch로 이동하도록 하는 역할을 하며, 이전 파일의 상태로 복원하도록 할 수 있는 역할을 한다.*
 
다음은 checkout 명령어의 옵션이다.

|옵션|설명|
|--|--|
|-b 새로운 branch이름 원격저장소의 branch|앞의 branch이름대로 새로운 branch를 형성하고, 이 branch를 원격저장소에 등록한다.|
|-f| 강제로 명령을 수행한다.|
|-q|메세지를 출력하지 않고 명령을 수행한다.|

작업자(저자)는 -b 옵션을 가장 많이 사용할 것이라 예상한다. 

그이유는 위의 작업처럼 신규 브랜치를 생성하고 원격 저장소의 브랜치와 연결하도록 하는 작업을 자주 사용하는데, 명령어를 여러개 사용하지 않고도 옵션을 통해 한번에 작업을 수행할 수 있개 한다는 점이 훨씬 유용하기 때문이다. 

----


# clone

> 구현 방법: **$ git clone 저장소URL 로컬저장소** 

현재 저장소는 exp branch와 master branch, 총 2개의 branch로 분화된 상태이고, exp branch에 위치한다. 

문서를 최신 버전으로 업그레이드 하기 위해 다른 문서로부터 온 코드가 필요한 상태이다. 

exp branch에 이 코드를 통한 새 파일을 담을 것 계획이다. 


<img width="437" alt="git clone" src="https://user-images.githubusercontent.com/81100851/117419829-f2798d80-af57-11eb-9a72-634e91a5dedb.png">

먼저, Github로 가서 필요한 코드를 담고 있는 저장소 URL을 복사하였다. 

이 URL을 이용하여 Github의 코드를 만들었다.


**요약 및 정리**

*git clone 명령어는 다른 저장소로부터의 코드를 복제하는 역할을 한다.*
*즉, 다른 작업자의 코드를 가져와 적용하는 작업에 필수적인 명령어이다.*

---

복제 작업을 진행한 이후, 작업자는 exp branch에 새 파일 extention.md를 만들었다

Github의 다른 저장소에서 복제한 최신 코드를 반영하여 extention.md를 수정하였고 

add 명령어와 commit 명령어를 사용하여 스테이지 영역에 올리고 커밋하는 작업까지 수행하였다. 

<img width="442" alt="git commit1" src="https://user-images.githubusercontent.com/81100851/117426843-59e70b80-af5f-11eb-8ab3-db4748dffb1b.png">

<img width="437" alt="git checkout branch merge branch" src="https://user-images.githubusercontent.com/81100851/117427155-b4806780-af5f-11eb-8943-bf16319c9a3a.png">

작업자는 exp branch에서 master branch로 이동한 후, master branch에서 exp branch와 merge를 시도하였다. 

*자세한 설명은 아래 명령어를 설명하면서 추가하도록 할 것이다.*
.
.
.
.


# merge

> 구현 방법: **$ git merge branch명**

위의 이미지를 살펴보면, 

현재 작업자는 checkout 명령어를 이용하여 exp branch에서 master branch로 이동하였다. 

exp branch 작업이 성공적으로 이루어 졌기 때문에 작업자는 이를 masdter branch에 반영할 계획이다. 

작업자는 exp branch와 master branch의 병합을 시도하여 하나의 파일로 소스를 통합하기 위해 merge 명령어를 사용한다. 

**요약 및 정리**

*merge 명령어는 서로 다른 branch를 통합하여 하나의 파일로 코드를 병합하도록 하는 역할을 한다.*

다음은 merge 명령어의 옵션이다. 

|옵션|설명|
|--|--|
|-m|메세지를 설정한다|
|-squash|브랜치의 로그를 삭제한다|

현재 작업자(저자)는 -squash 옵션을 사용할 가능성이 높다. 

병합을 시도하는 경우, branch의 로그가 남아 여러 파일을 수정한 작업자에게는 파일을 헷갈리게 하여 작업을 실수하도록 유발할 수 있기 때문에 merge 이후 로그를 없애 이미 필요가 없어진 파일에 고려하지 않도록 할 수 있기 때문이다. 

---


# reset 

> 구현 방법: **$ git reset --hard**

현재 exp branch와 master branch의 최신 파일을 병합한 상태이다. 

그러나 작업자는 아직 두 branch를 병합하면 안되는 상태임을 merge 명령어를 사용한 이후에 깨달았다. 

그러므로 merge 명령어를 사용하기 이전의 상태(부모 커밋)로 되돌아가도록 하기 위해 reset 명령어를 사용한다. 


<img width="437" alt="git reset " src="https://user-images.githubusercontent.com/81100851/117428899-75531600-af61-11eb-8e88-70bc45dd1856.png">


작업자는 git reset --hard 되돌아 갈 위치를 선정하여 merge 이전의 상태로 돌아갔다. 

이때 되돌아간다는 의미에서 주의해야 하는데, 작업자가 사용한 reset --hard는 이전의 커밋으로 되돌아가면서 데이터를 삭제시키기 때문이다. 

**요약 및 정리**

*reset 명령어는 merge commit을 없애는 기능을 한다고 정리할 수 있다.*
 

reset 명령어는 3가지 옵션을 갖는다. 

|옵션|설명|
|--|--|
|--hard|데이터를 삭제하면서 HEAD를 이동시켜 인덱스를 HEAD가 가리키는 상태로 만든다.| 
|--soft|HEAD를 이동시킨다.|
|--mixed| HEAD를 이동시킨후 인덱스를 HEAD가 가리키는 상태로 만든다. 이동시킨 이후 HEAD의 다른 점을 출력한다|

작업자(저자)는 위의 Git 실습한 이미지처럼 --hard 옵션을 자주 사용할 것이다. 

다른 옵션은 되돌아갈때 잘못 수행했던 커밋을 다루진 않는다. 하지만 --hard는 잘못 수행했던 커밋을 삭제하므로서 이전 커밋으로 되돌아가기 때문이다. 

저자는 --hard 옵션을 사용하므로서 되돌아간다는 reset 명령어의 의미에 더 부합한다고 생각한다. 

그러나 그만큼 reset 명령어 사용에 주의해야 할 것을 명심해야 할 것이다. 

---


작업자는 reset 명령어를 통해 merge 이전의 상태로 되돌린 이후, 

markdown.md 파일을 수정하였고, 

add 명령어 commit 명령어를 사용하여 파일을 스테이지 영역에 올리고, fifth 라는 커밋 메세지를 생성하며 커밋하였다. 

<img width="434" alt="git add commit branch merge" src="https://user-images.githubusercontent.com/81100851/117432906-d7157f00-af65-11eb-923a-c6f4029cbef7.png">

이제 작업자는 merge 명령어를 사용하여 branch를 병합할 계획이다. 

.
.
.
.

# log

> 구현 방법: **$ git log**

현재 여러 파일을 커밋해놓은 상태이고, 원격 저장소에도 파일을 올린 상태이다. 

merge 명령어로 병합하기 전에, 이전의 작업 실수를 반복하지 않기 위해 

작업자는 log 명령어를 사용하므로써 작업이 원하는대로 잘 수행되고 있는지 중간 점검을 하도록 할 것이다. 

<img width="449" alt="git log1" src="https://user-images.githubusercontent.com/81100851/117433773-d0d3d280-af66-11eb-8aa2-a3ba108199c8.png">

작업자는 git log 명령어의 --oneline 옵션을 사용하여 log 정보(파일명과 커밋정보)가 한줄로 나타나도록 할 것이다.


**요약 및 정리** 

*log 명령어는 Git의 이력 관리 역할을 한다.* 

다음은 log 명령어의 옵션이다. 

|옵션|설명|
|--|--|
|--stat|log 정보(주소, 이메일 주소, 날짜, 메세지, Author)을 작업 순대로 각각 나타내준다.|
|--online|log 정보를 요약하여 아주 간단히 한 줄로 나타내준다.|

앞서 작업자(저자)가 --oneline 옵션을 수행한 것처럼, 앞으로 저자는 --oneline 옵션을 자주 사용 할 것이다. 

작업자는 중간 점검을 위해 log 명령어를 사용하는 것이기 때문에. 나타낼 log 정보가 많을 수록 확인하는데 스크롤을 요해서 작업에 혼란을 야기함을 경험하였다. 

또한 작업을 수행하는데 주로 commit정보와 파일명 만 이용하는 경우가 잦았다.

--oneline 옵션은 한줄로 나타내주기 때문에 작업 효율을 높여줌을 경험하였기 때문이다. 

---

# pull

> 구현 형태: **$ git pull origin master**

현재 작업자는 최신 파일들을 merge 한 상태이다. 

작업 과정에서 github 원격저장소에 올린 버전의 파일이 필요함을 느꼈다.

작업자는 pull 명령어를 사용하여 원격 저장소에 올린 파일을 가져올 것이다. 

<img width="439" alt="git pull" src="https://user-images.githubusercontent.com/81100851/117435341-b7338a80-af68-11eb-92ab-d3bce11b59ef.png">

작업자는 origin으로 등록된 원격저장소에 있는 파일을 가져오도록 하기 때문에 URL 사용하는것 대신에 origin을 사용한 것이다. 

본래, pull할 코드가 담긴 저장소의 URL을 사용하여 git 저장소로 가져오면 된다. 

저자는 clone 명령어와 pull 명령어가 유사하다는 점을 강조하고 싶다.  

즉, 다른 개발자들이 명령어 push를 이용하여 등록한 파일을 명령어 pull을 이용하여 나의 git에 적용가능하며, 나의 버전을 업데이트 시킬 수 있다. 

**요약 및 정리**

*pull 명령어는 Github 저장소에 있는 최신 코드를 git 저장소로 가져오도록 하는 역할을 한다.*

---

작업자는 앞서 계획한대로 exp branch에 있는 코드와 master branch에 있는 코드를 병합하는데 성공하였다.

저자는 origin 이름으로 저장된 Github의 원격 저장소로 master의 내용을 업로드 하였다. 

<img width="442" alt="git push origin master" src="https://user-images.githubusercontent.com/81100851/117437338-01b60680-af6b-11eb-82be-f2d609c6d4bc.png">

이후 작업자는 이 버전의 tag를 설정할 계획이다. 
.
.
.

# tag 

> 구현 방법: **$ git tag 태그명** 

현재 git에는 tag가 저장되어있지 않은 상태이다.

작업자는 tag를 사용하여 앞으로의 버전을 구분해나갈 계획이다.

tag 명령어를 사용하여 현재의 HEAD를 버전 1.0로 저장하도록 한다. 

<img width="443" alt="git tag1" src="https://user-images.githubusercontent.com/81100851/117437622-6ffac900-af6b-11eb-8cc4-4d890207da2d.png">


**요약 및 정리**

*tag 명령어는 HEAD가 위치한 파일에 tag를 생성하도록 하는 역할을 한다.*

다음은 tag 명령어의 옵션이다.

|옵션|설명|
|--|--|
|-m|tag를 남길때 메세지를 함께 생성할 수 있다.|
|-a|Annotated 태그를 생성할 수 있다.|

작업자(저자)는 -m 옵션을 자주 사용할 것으로 예상된다. 

tag를 이용하여 버전을 분류하도록 할 것이기 때문에, 메세지를 생성하여 작업자가 쉽게 어떤 버전인지 알아볼 수 있도록 할 수 있기 때문이다. 



---

# rebase 

> 구현 방법: **$ git rebase** 

현재 작업자의 계획대로 완성된 결과물에 대해 1.0이라는 tag를 생성한 상태이다.

작업자는 앞으로의 버전 개발을 생각하여 one이라는 extention.md 파일의 commit 명을 extention1으로 변경하기를 수행하기 위해 rebase 명령어를 사용한다.

<img width="398" alt="git rebase1" src="https://user-images.githubusercontent.com/81100851/117442118-4fce0880-af71-11eb-817b-13364dab75dd.png">

먼저,

작업자는 commit 명을 변경하기 위해 rebase -i --root를 사용하였다. 

<img width="437" alt="git rebase2" src="https://user-images.githubusercontent.com/81100851/117442129-5492bc80-af71-11eb-8050-19638765dde1.png">

rebase 명령을 실행하기 위해 자동으로 위와 같은 창이 뜬다.

명령어 입력을 가능케 하도록 i 를 눌러준후, 

commit 정보 앞에 써진 초록색의 PICK 대신에 reword를 입력해주고 one 이라는 commit 명 대신에 extention1을 입력한다. 

입력 후 ESC : wq 를 차례대로 눌러주어 빠져나온다. 

<img width="433" alt="git rebase3" src="https://user-images.githubusercontent.com/81100851/117442143-58264380-af71-11eb-941d-45a9d7f75acb.png">

작업자는 이후 자동으로 위와 같은 창이 뜸을 경험할 것이다. 

작업자는 one 대신 extention1을 입력해준 후, 

파란색 글씨로 된 rebase 설정을 확인한다. 

이때 본 작업자는 다른 commit을 건들이지 않고, rebase progress를 commit 정보 420e626에만 reword할 것이므로 작업자의 계획 조건에 부합하도록 수정해준다. 

<img width="430" alt="git rebase4" src="https://user-images.githubusercontent.com/81100851/117442155-5b213400-af71-11eb-8189-e52b43c6c0fa.png">

rebase 명령어를 수행한 이후 log 정보를 확인하여 commit 명이 변경되었음을 확인할 수 있다. 

**요약 및 정리**

*rebase 명령어는 (1) commit 메세지를 수정하는 역할 (2) commit을 합치는 역할 (3) commit을 삭제하는 역할을 하므로서 이전 작업에 대한 작업을 할 수 있다.*

다음은 rebase 명령어의 옵션이다.

|옵션|설명|
|--|--|
|-i|interactive 모드를 통해 commit 정보를 수정하는 작업을 하도록 한다|
|--onto|rebase 작업을 분리하여 한번에 여러 rebase 단계를 거칠 수 있다.|


|번호|명령어| 사용여부|해당내용으로 이동|
|--|--|--|--| 
|1.| init|O| [init](#init)|
|2.| stauts|O| [status](#status)|
|3.| remote |O| [remote](#remote)|
|4.| add|O|  [add](#add)|
|5.| commit|O| [commit](#commit)|
|6.| push|O| [push](#push)|
|7.| config|O| [config](#config)|
|8.| branch|O| [branch](#branch)|
|9.| checkout|O| [checkout](#checkout)|
|10.| clone|O| [clone](#clone)|
|11.| merge |O| [merge](#merge)|
|12.| reset--hard|O| [reset](#reset)|
|13.| log |O| [log](#log)|
|14.| pull|O| [pull](#pull)|
|15.| tag|O| [tag](#tag)|
|16.| rebase|O| [rebase](#rebase)|

