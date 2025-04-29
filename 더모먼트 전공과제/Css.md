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
1.**태그 선택자**: HTML의 태그 이름을 그대로 쓰는것이다.
  ```
p {
  color: blue;
}
```
<br><br>

2.**클래스 선택자**: 클래스명 앞에 .점을 붙여서 선택한다.<br><br>
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

3.**아이디 선택자**: 아이디명 앞에 #샵을 붙여서 선택한다.<br><br>
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

4.**전체 선택자**: * 를 사용하면 모든 요소에 적용된다.
```
* {
  margin: 0;
  padding: 0;
}
```
<br><br>

5.**그룹 선택자**: , 콤마를 써서 여러 요소를 한 번에 선택할 수 있다.
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

글꼴(Font)
------------------
1. 글자 종류 설명
 ```
body {
  font-family: 'Arial', sans-serif;
}
```
<br>

2. 글자 크기 조절
 ```
p {
  font-size: 16px;
}
```
<br>

3. 글자 굵기 조절
```
h1 {
  font-weight: bold; 
}
```
<br>

4. 글자 스타일
```
em {
  font-style: italic;
}
```
<br>
<br>

색상 스타일링
-------------
1. 글자 색상 바꾸기
  ```
  h2 {
  color: blue;
}
 ```
<br>

2. 배경 색상 바꾸기
```
div {
  background-color: lightgray;
}
```
<br>

 배경 스타일링
 ------------
 1. 배경 이미지 넣기
```
 body {
  background-image: url('https://example.com/image.jpg');
}
```
<br>

2. 배경 크기 조정
```
body {
  background-size: cover;
}
```
<br>

3. 배경 반복 여부
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
Box Model이란?


