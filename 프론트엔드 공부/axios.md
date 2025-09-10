# Axios

### Axios란 무엇일까?

Axios는 **Promise기반**의 Http 비동기 통신 라이브러리이다.
<br>
<br>
<br>

### Axios의 특징들

**장점**:

- Promise의 기반이기 때문에 비동기의 작업을 직관적이고 더 간단하게 쓸수있다.

- 또한 다른것들은 JSON 데이터 형태로 일일이 변환해야하지만 Axios는 자동으로 데이터를 Json으로 반환해준다.

- 또한 **Interceptors**를 지원한다.
  여기서 Intercepters란? 원래 코드가 실행되기 전/후에 끼어들어서 추가 작업을 할 수 있는거라 생각하면 된다!

- 그리고 비동기 요청을 취소할수도 있어서 필요 없는 요청을 줄일 수 있다.

- 또한 타임아웃도 설정이 가능해서 설정한 시간 이내에 응답이 없으면 요청 취소도 가능하다.
  <br>
  <br>

**단점**:

- 외부 라이브러리이기 때문에 직접 프로젝트에 추가해야해서 번거로울 수 있다
- 크기가 일반적인 fetch에 비해 Axios가 더 크다.
  <br>
  <br>

실습 예시

```js
import axios from 'axios'; //Axios 라이브러리를 불러옴

axios
  .get('https://github.com/seoxeon09')
  .then((response) => {
    console.log('요청이 성공적으로 되었습니당', response.data);
  }) //성공시 성공 메세지 뜨도록 설정
  .catch((error) => {
    console.error('요청이 실패했습니당', error);
  }); //실패시 에러 메세지 뜨도록 설정
```

Date: 2025-09-10
