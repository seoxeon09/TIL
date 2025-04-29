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

#### 글자 종류 설명
 ```
body {
  font-family: 'Arial', sans-serif;
}
```
<br>

#### 글자 크기 조절
 ```
p {
  font-size: 16px;
}
```
<br>

#### 글자 굵기 조절
```
h1 {
  font-weight: bold; 
}
```
<br>

#### 글자 스타일
```
em {
  font-style: italic;
}
```
<br>
<br>

색상 스타일링
-------------
#### 글자 색상 바꾸기
  ```
  h2 {
  color: blue;
}
 ```
<br>

#### 배경 색상 바꾸기
```
div {
  background-color: lightgray;
}
```
<br>
<br>

 배경 스타일링
 ------------
 
 #### 배경 이미지 넣기
```
 body {
  background-image: url('https://example.com/image.jpg');
}
```
<br>

#### 배경 크기 조정
```
body {
  background-size: cover;
}
```
<br>

#### 배경 반복 여부
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

> **[Margin]** :   바깥 여백 (가장 바깥)을 말한다.<br><br>
> **[Border]** :  테두리이다.<br><br>
> **[Padding]** :  안쪽 여백 (내용과 테두리 사이)를 의미한다.<br><br>
> **[Content]** : 실제 내용 (텍스트, 이미지 등)을 적는다.<br><br><br>

![img_css_boxmodel](https://github.com/user-attachments/assets/96b3e302-16d8-47b7-9705-a3e4cbf20f9f)
<br>
<br>
<br>

왜 중요할까?
-------------
>- 콘텐츠가 너무 붙어보이거나, 너무 멀어보이면 보기 안 좋다.<br>
이럴 때 padding, margin을 조절해서 보기 좋게 배치할수 있다.<br><br>
>- 화면이 깨지지 않게 하거나, 다른 요소랑 안 겹치게 만들 때도 필수이다.





