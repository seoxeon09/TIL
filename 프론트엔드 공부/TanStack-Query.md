# TanStack Query

## TanStack Query란 무엇일까?

**TanStackQuery**는 서버로부터 데이터 가져오기, 데이터 캐싱, 캐시 제어 등 데이터를 쉽고 효율적으로 관리하는 라이브러리이다.

- 원래 이름은 React Query였지만 다른 프레임워크에서도 사용이 가능해 TanStackQuery로 이름이 바꼈다.
  <br>
  <br>

TanStack Query의 기능?

- 데이터 가져오기 및 캐싱
- 동일한 요청을 중복
- Fresh한 데이터 유지
- 요청 실패시 자동으로 갱신되도록 설정

<br>
<br>

### 데이터 캐싱

TanStack Query에서 데이터를 가져올때는 쿼리 키(query key)를 사용한다. 쉽게 말해 캐쉬된 데이터와 비교하여 새로운 데이터를 가져올지 결정한다.

### useQuery

- useQuery란?
  가장 기본적인 쿼리 훅으로, 컴포넌트에서 데이터를 가져올 때 사용합니다.

### queryKey

- queryKey란?
  쿼리를 식별하는 고유한 값이며 배열 형태로 쓰입니다.
  <br>
  <br>

예시 코드

```js
//단일 아이템 쿼리 큐
useQuery({ queryKey: ['hello'] });

//다중 아이템 쿼리 큐
useQuery({ queryKey: ['hello', 'world', 123, { a: 1, b: 2 }] });
```

### queryFn

- 쿼리 함수는 데이터를 가져오는 비동기 함수로, 꼭 데이터를 반환하거나 오류를 올려야한다. 올려진 오류는 반환되는 error 객체로 확인할 수 있다.

### select

- 선택 함수를 사용하면 가져온 데이터를 선택할수 있다. 쿼리 함수가 반환하는 데이터를 인수로 받아 선택 함수에서 처리하고 반환하면 최종 데이터가 된다.
  <br>

Date: 2025-09-15
