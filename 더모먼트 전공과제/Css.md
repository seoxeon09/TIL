Css의 기본 문법 및 Selecter
============================
CSS는 HTML 요소에 **스타일(디자인)** 을 입혀주는 언어이다.<br>
CSS 문법 기본 형태:

```
선택자 {
  속성: 값;
}
```
>- **선택자** : 스타일을 적용할 대상을 고르는것이다. (ex: h1, .menu, #title)<br>
>- **속성** : 꾸미고 싶은 스타일의 종류이다. (ex: color, font-size, font-family, background-color)<br>
>- **값** : 그 스타일의 구체적인 설정이다. (ex: 분홍색, 20px, 파란 배경)
<br>
<br>
적용 예시:

```
h1 {

 font-size: 20px;
 text-align: center;
 color: tomato;

 }
```
<br>
<br>
<br>
<br>



Selecter(선택자)의 종류와 사용법
--------------------------------
### 태그 선택자<br>
HTML의 태그 이름을 그대로 쓰는것이다.
  ```
p {
  color: blue;
}
```
<br><br>

### 클래스 선택자<br>
클래스명 앞에 .점을 붙여서 선택한다.<br><br>
Html 예시:
```
<p class="text">Hello</p>
```
Css 예시:
```
.text {
  font-size: 20px;
}
```
<br><br>

### 아이디 선택자<br>
아이디명 앞에 #샵을 붙여서 선택한다.<br><br>
Html 예시:
```
<p id="special">Hi</p>
```
Css 예시:
```
#special {
  color: green;
}
```
<br><br>

### 전체 선택자<br>
* 를 사용하면 모든 요소에 적용된다.<br>
```
* {
  margin: 0;
  padding: 0;
}
```
<br><br>

### 그룹 선택자<br>
, 콤마를 써서 여러 요소를 한 번에 선택할 수 있다.<br>
```
h1, h2, p {
  color: purple;
}
```
<br>
<br>
<br>
<br>

Css 기초 스타일링
=================
<br>

글꼴(Font)
------------------

### 글자 종류 설명
 ```
body {
  font-family: 'Arial', sans-serif;
}
```
<br>

### 글자 크기 조절
 ```
p {
  font-size: 16px;
}
```
<br>

### 글자 굵기 조절
```
h1 {
  font-weight: bold; 
}
```
<br>

### 글자 스타일
```
em {
  font-style: italic;
}
```
<br>
<br>

색상 스타일링
-------------
### 글자 색상 바꾸기
  ```
  h2 {
  color: blue;
}
 ```
<br>

### 배경 색상 바꾸기
```
div {
  background-color: lightgray;
}
```
<br>
<br>

 배경 스타일링
 ------------
 
 ### 배경 이미지 넣기
```
 body {
  background-image: url('https://example.com/image.jpg');
}
```
<br>

### 배경 크기 조정
```
body {
  background-size: cover;
}
```
<br>

### 배경 반복 여부
```
   body {
  background-repeat: no-repeat;
}
```
<br>
<br>
<br>
<br>

Box Model
===========
Box Model이란? <br>
웹페이지에서 모든 Html 요소가 **네모난 상자(box)** 처럼 생겼다고 생각하는 모델이다.<br><br>
이 박스들은 *총 4부분* 으로 나뉘어져 있다.<br><br>
![img_css_boxmodel](https://github.com/user-attachments/assets/96b3e302-16d8-47b7-9705-a3e4cbf20f9f)
<br>
<br>

> **[Margin]** :   다른 요소와의 바깥 간격으로 박스끼리 떨어뜨리고 싶을때 사용한다.<br><br>
> **[Border]** : 요소를 감싸는 테두리로, 선 색, 두께 등을 조절할 수 있다.<br><br>
> **[Padding]** :  콘텐츠와 테두리(border) 사이의 공간으로 콘텐츠에 여유 공간을 주고 싶을때 쓴다.<br>
→ 배경색이 들어가면 패딩에도 색이 들어간다.<br><br>
> **[Content]** : 바깥 여백 (가장 바깥)을 말한다. 실제 내용이 들어가는 부분이다.<br>
예: &lt;p&gt; 안녕 &lt;/p&gt; 이라 적으면 "안녕" 글자가 있는 부분이라 생각하면 된다.

<br>
<br>

예시 코드
```
.box {
  width: 200px;
  height: 100px;
  padding: 20px;
  border: 5px solid black;
  margin: 30px;
}
```

왜 중요할까?
-------------
>- 콘텐츠가 너무 붙어보이거나, 너무 멀어보이면 보기 안 좋다.<br>
이럴 때 padding, margin을 조절해서 보기 좋게 배치할수 있다.<br><br>
>- 화면이 깨지지 않게 하거나, 다른 요소랑 안 겹치게 만들 때도 필수이다.<br><br>

<br>
<br>
<br>
<br>
<br>

레이아웃(layout)
=================

레이아웃: 웹 페이지에서 요소(글, 이미지, 버튼 등)이 어디에, 어떻게 배치되어 있는지를 정하는 구조를 말한다.<br>
쉽게 말하면, 웹 페이지의 "뼈대" 또는 "배치 설계도" 같은거라 생각하면 된다. <br><br>
<br>


필요한 이유
------------
>- 보기 좋은 페이지 만들기 위해서
>- 사용자들이 편하게 사용할 수 있도록 구성
>- 모바일/태블릿 등 다양한 화면에 맞게 자동 조절 가능
<br>
<br>
<br>


레이아웃 도구들
--------------

### 1. display(디스플레이) 
**디스플레이란 요소가 어떤 방식으로 배치될지 정하는 속성이다.**
<br>
<br>

![1_eTM7rZjWEbhcn9HHNn7l6Q](https://github.com/user-attachments/assets/51b574e9-ec75-4627-88a8-a235f0a6fedd)

<br>

>- **block** :	한 줄을 다 차지한다.	ex) &lt;div&gt;, &lt;p&gt; <br><br>
>- **inline** :	글처럼 옆으로 나란히 놓는것을 의미한다. ex) &lt;span&gt;, &lt;a&gt; <br><br>
>- **inline-block** :	옆으로 나란히 + 크기 조절 가능 버튼 만들 때 자주 쓴다. <br><br>
>- **flex** :	유연하게 정렬 쉽게 정렬을 해준다. <br><br>
>- **grid** :	격자처럼 정렬 표처럼 칸 나누는 느낌이다. <br><br>
<br>
<br>
<br>
<br>

### 2. position(포지션)
**요소를 어디에 둘지 정하는 방식이다.**
<br>
<br>

![image](https://github.com/user-attachments/assets/f503645f-2764-4eb9-9b8b-7d41ff32f80f)

<br>


>- **static** :	기본값, 흐름대로 배치	아무 것도 안 하면 이 상태이다.<br><br>
>- **relative** : 기준점에서 조금 이동	위치 조정할때 쓴다.<br><br>
>- **absolute** : 정확한 위치로	버튼을 특정 위치에 고정할때 쓴다.<br><br>
>- **fixed** :	화면에 고정을 하여	스크롤해도 안 사라지는 메뉴이다.<br><br>
>- **sticky** :	스크롤할 때 붙어있다가 내려가는	상단바 만들 때 유용하다.<br><br>
<br>
<br>
<br>
<br>

### 3. flexbox(플랙스 박스)
**가로 또는 세로로 요소를 정렬할때 쓰인다.**
<br>
<br>

*flex container 만들기*
```
.container {
  display: flex;
}
```
<br>

![a-1665382286109-2x](https://github.com/user-attachments/assets/b295ae10-cc60-464b-9d24-ea02aa35f5e9)

<br>

>- **justify-content** : 주축 방향 정렬하기 (가로 정렬)<br><br>
>- **align-items** :	교차축 정렬하기 (세로 정렬)<br><br>
>- **flex-direction** :	방향 바꾸기 (row, column 등)<br><br>
>- **gap** : 요소 사이 간격 조절하기<br><br>















