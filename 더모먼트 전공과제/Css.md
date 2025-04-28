Css의 기본 문법 및 Selecter
-----------------------------
CSS는 HTML 요소에 **스타일(디자인)** 을 입혀주는 언어이다.<br><br>
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

Selecter(선택자)의 종류와 사용법
--------------------------------
1.태그 선택자: HTML의 태그 이름을 그대로 쓰는것이다.
  ```
p {
  color: blue;
}
```


