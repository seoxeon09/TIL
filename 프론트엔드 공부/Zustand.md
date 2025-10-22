# Zustand

## Zustand란 무엇일까?

Zustand는 React 프로젝트에서 사용하는 상태 관리 라이브러리이다.

- 쉽게 말하자면 폴더가 만약 App - Parent - Child 이런식으로 있다고 가정해보자.
  <br> **App**에서 **Child**에게 Props를 주고싶다면 중간 컴포넌트인 **Parent**도 Props를 받아야한다.
  <br>
  <br>
  하지만 이게 문제점이 폴더가 많으면 여러 데이터를 계속 Props로 받아야하는데 이러면 중첩이 생기고 많이 복잡해질수 있다.
  <br>
  <br>

### 이를 위한 해결방법은 무엇일까?

앞서 내가 말했던것처럼 여러 파일이 있으면 문제점이 상당히 많다. 이거를 보완하기 위해 만들어진게 바로 **context API**와 **Zustand**가 있다.<br>

그 중 오늘은 제일 많이 쓰는 Zustand에 대해 알아보겠다.

**Zustand**는 아까 말했듯이 React 프로젝트에서 사용하는 상태 관리(Store라고도 불린다)라이브러리이다.

Zustand나 Context API는 상위 폴더에서 하위 폴더로 이동할때 Props 데이터 받는 구조를 더 간결하게 해준다. 쉽게 코드로 예시를 들어보겠다.

```js
function GrandChild({ message }) {
  return <p>{message}</p>;
}

function Child({ message }) {
  return <GrandChild message={message} />;
}

function Parent({ message }) {
  return <Child message={message} />;
}

function App() {
  return <Parent message="안녕, 나는 App이야!" />;
}
```

- 이 코드를 살펴보면 Props를 받을 필요없는 Child와 Parent까지 message를 쓴다. 지금은 코드가 그리 길진 않지만 나중에는 코드가 길어져 가독성이 낮아진다.

이 코드를 Zustand 라이브러리를 활용하여 바꿔보면

```js
import create from 'zustand';

const useStore = create(() => ({ message: '안녕 나는 서연이야' }));

function GrandChild() {
  const message = useStore((state) => state.message);
  return <p>{message}</p>;
}
```

이런식으로 아주 간단하게 될 수 있다.

하지만 만약 파일이 그리 많지 않다면 굳이 Zustand나 Context API를 쓰지 않아도 된다. 오히려 더 복잡해질수가 있다. 그러므로 상황에 따라 어떤걸 쓸건지 혹은 안 써도 되는건지 잘 파악하면서 써야한다.

Date: 2025-10-22
