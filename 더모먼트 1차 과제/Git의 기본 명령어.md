Git의 기본 명령어 사용법들
 =====================
 <br>
 
git init은 무엇일까?<br>
-------------
>- Git을 로컬 저장소에서 만들기 위해서는 Git bash라는 프롬포트에서 ***git init***을 입력하면 .git이라는 파일이 생성된다.<br>
>- 이 파일은 버전에 대한 정보를 담고 있다.<br>
>- 또한 파일이 추가 삭제 되는걸 자동으로 스스로 감지할수 있다.<br>
>- **git init**의 약자는 *initialize*인데 초기화라는 뜻이다.<br>

>- **git add**는 작업 디렉토리 상의 변경 내용을 스테이징 영역에 추가하기 위해 사용하는 명령어이다.<br>
>- **git add**를 실행하면 .git폴더 내부에는 index파일과 objects폴더 아래에 파일이 하나 생기게 된다.<br>
<br>
<br>
<br>
<br>

Index
----------
> **index**: 현재 **스테이징 영역에 존재하는 파일**을 의미하는데 즉 *commit*하기를 대기하는 파일들의 목록이다.
<br>
<br>
<br>
<br>

Objects
---------
> **objects**: 스테이징 영역에 올라온 파일에 대한 내용이 생성되거나 커밋 내용이 생성되는 객체 폴더이고,<br>
하위 폴더에는 각각의 고유한 문자열로 저장이 된다.<br>
<br>
<br>

Commit
-------
> commit은 의미있는 변경 작업들을 **저장소에 기록** 시키는것을 말한다.<br>
한마디로 commit 버튼을 눌러야 저장소에 기록 시킬수 있다.<br>
<br>
<br>

Push와 Pull
------------
> **push**는 내가 만든 코드를 **깃허브에 올리고 싶을때** push를 하면 된다.<br>
그러면 반대로 다른 사람이 만든 코드를 **내 컴퓨터로 가져오고 싶을때**는?<br>
그때 **pull**을 사용하면 된다.<br>
쉽게 얘기하면 push <-> pull
