JS 기본 문법
===============

## 변수
**변수(Variable)** 는 말 그대로 변할 수 있는 값을 담는 상자이다.<br>

예시: 
```
let age = 17;
```

여기서 age라는 변수에 16이라는 값을 넣었으니<br>
이제 age를 출력하면 16이 나오게된다.<br>
<br>
<br>

## 변수를 선언하는 방법
자바스크립트에서는 변수를 **3가지** 키워드로 만들 수 있다.<br>

>- **var** :	재선언 가능, 재할당 가능, 블록 범위가 아니다, 요즘엔 거의 쓰지 않는다.<br>
>- **let** : 재선언 불가능, 재할당 가능, 블록 범위<br>
>- **const** :	한 번 정하면 바꿀수 없는 값<br>
<br>
<br>
<br>
<br>
<br>

## 조건문
**조건문**은 어떤 조건이 맞으면(참이면) 실행을 하고 아니면(거짓이면) 다른일을 실행하는 것이다.<br>

조건문의 기본 구조:
```
if (조건) {
  // 조건이 참일 때 실행할 코드
} else {
  // 조건이 거짓일 때 실행할 코드
}
```
<br>

예시: 
```
let score = 90;

if (score >= 80) {
  console.log("A");
} else {
  console.log("B");
}

```
<br>
<br>
<br>

+ 삼항 연산자?
**삼항 연산자**는 기존의 조건문을 더 간단하게 쓰는것이다.<br>

  삼항 연산자의 기본 구조:
  ```
  (조건) ? 참일 때 : 거짓일 때
  ```
  
  예시:
  ```
  let score = 90;
  let result = (score >= 90) ? "합격" : "불합격";
  console.log(result); // "불합격"
  ```
<br>
<br>
<br>
<br>
<br>

## 반복문
**반복문**은 특정 작업을 여러번 반복해서 수행하도록하는 것이다.<br><br><br>

## for문
가장 기본적이고 자주 쓰이는 반복문이다.<br><br>

입력:
```
for (let i = 1; i <= 5; i++) {
  console.log(i);
}
```
>- let i = 1 → 변수 i를 1로 시작하고
>- i <= 5 → i가 5보다 작거나 같을 동안 반복하고
>- i++ → 한번 실행할 때마다 i를 1씩 늘린다.<br>

출력:
```
1
2
3
4
5
```
<br>
<br>

## while문
조건이 참일동안 계속 반복한다. while문은 언제 끝날지 확실하지 않을때 좋다.<br><br>

입력:
```
let i = 1;

while (i <= 5) {
  console.log(i);
  i++;
}
```
출력:
```
1
2
3
4
5
```
<br>
<br>

## do...while문
while문과 비슷하지만 무조건 한번은 실행된다.<br><br>

입력:
```
let i = 1;

do {
  console.log(i);
  i++;
} while (i <= 5);
```
출력:
```
1
2
3
4
5
```
<br>
<br>

## for...of문
**배열 안의 값**들을 하나씩 꺼내서 반복할때 쓴다.<br><br>

입력:
```
let fruits = ["청포도", "레몬", "딸기"];

for (let fruit of fruits) {
  console.log(fruit);
}
```
출력:
```
청포도
레몬
딸기
```
<br>
<br>

## for...in문
**객체 안의 키(이름들)** 을 꺼내서 반복한다.<br>
**객체에서 사용한다.**<br><br>

입력:
```
let user = {
  name: "서연",
  age: 17,
  hobby: "잠.."
};

for (let key in user) {
  console.log(key + ": " + user[key]);
}
```
출력:
```
name: 서연
age: 17
hobby: 잠..
```
<br>
<br>
<br>


+ **break**: 반복을 멈추고 나감<br>
+ **continue**: 이번 반복만 건너뛰고 다음 반복으로 넘어감<br><br>


입력:
```
for (let i = 1; i <= 5; i++) {
  if (i === 3) {
    continue; // 3일 때는 건너뜀
  }
  console.log(i);
}
```
출력:
```
1
2
4
5
```
<br>
<br>
<br>
<br>

 ## 함수(Function)
함수는 어떤 일을 묶어서 이름 붙여놓은 것이다. 필요할때마다 함수 이름으로 불러서 실행한다.<br><br>

함수 만드는법(선언):
```
function sayHello() {
  console.log("안녕!");
}
```
함수 사용하는법(호출):
```
sayHello(); // 결과: 안녕!
```
<br>
<br>

### 매개변수와 return

```
function add(a, b) {
  return a + b;
}

let result = add(3, 5); // result = 8
console.log(result);    // 8
```
>- `a, b`는 매개변수(입력값)<br>
>- `return`은 **결과(출력값)** 를 돌려주는 것이다.<br>
<br>
<br>
<br>
<br>

## 배열(Array)
배열은 여러 값을 **하나로 묶어서 저장**하는 상자이다. 값에는 숫자, 문자, 함수, 객체들이 들어갈수 있다.<br><br>

배열 만드는법:
```
let fruits = ["사과", "바나나", "딸기"];
```

배열에서 값 꺼내기:
```
console.log(fruits[0]); // 사과
console.log(fruits[1]); // 바나나
```
> 배열은 숫자 번호(index)가 0부터 시작한다.<br>
<br>
<br>

배열 값 추가/삭제:
```
fruits.push("포도");   // 맨 뒤에 추가
fruits.pop();          // 맨 뒤 제거
fruits.unshift("귤");  // 맨 앞에 추가
fruits.shift();        // 맨 앞 제거
```

배열 반복하기:
```
for (let fruit of fruits) {
  console.log(fruit);  // 하나씩 출력
}
```
<br>
<br>
<br>
<br>

## 객체(Object)
객체는 이름(key)과 값(value)을 짝지어서 저장하는 것이다. 쉽게 말해, 정보를 묶어서 표현하는 상자이다.<br><br>

객체 만드는법:
```
let user = {
  name: "서연",
  age: 17,
  hobby: "sleeping"
};
```

객체 값 꺼내기:
```
console.log(user.name);   // 서연
console.log(user["age"]); // 17
```
<br>
<br>

객체 값 추가/삭제:
```
user.job = "학생";       // 추가
user.age = 18;           // 변경
delete user.hobby;       // 삭제
```

객체 반복하기(for..in) :
```
for (let key in user) {
  console.log(key + ": " + user[key]);
}
```
<br>
<br>

|개념|설명|예시|
|------|---|---|
|함수|어떤 코드를 묶어서 사용|function sayHi() {...}|
|배열|여러 값을 순서대로 저장|["키위", "딸기"]|
|객체|이름(key)과 값(value) 저장|{ name: "서연", age: 17 }|

<br>
<br>
<br>
<br>
<br>

## DOM 선택자 및 조작
DOM은 웹 페이지의 구조(HTML)를 자바스크립트로 조작하는 방법이다.<br><br>

### 선택자(querySelector)
HTML에서 원하는 요소를 선택할 수 있다.<br><br>

Html
```
<p id="myText">안녕하세요</p>
```
Javascript
```
let text = document.querySelector("#myText");
console.log(text.innerText); // 안녕하세요
```
> `#id`, `.class`, `태그이름` 으로 선택할 수 있다.

<br>
<br>

### 내용 바꾸기(innerText, innerHTML)

Javascript
```
text.innerText = "반가워요!"; // 텍스트만 바꿈
text.innerHTML = "<strong>굵게!</strong>"; // HTML 태그도 가능
```
<br>
<br>
<br>
<br>

## 이벤트 처리 (addEventListener)
버튼을 클릭했을 때, 입력했을 때 어떤 동작을 하게 하는 코드이다.<br><br>

### 클릭 이벤트 예시
Html
```
<button id="btn">눌러봐!</button>
```
Javascript
```
let btn = document.querySelector("#btn");

btn.addEventListener("click", function () {
  alert("버튼을 눌렀어요!");
});
```
<br>

### 입력 이벤트 예시
Html
```
<input id="nameInput" placeholder="이름을 입력하세요">
```
Javascript
```
let input = document.querySelector("#nameInput");

input.addEventListener("input", function () {
  console.log("입력 중:", input.value);
});
```



