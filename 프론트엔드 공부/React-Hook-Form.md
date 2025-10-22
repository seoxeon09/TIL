# React Hook Form

## React Hook Form이란?

React에서 폼을 쉽게 만들고, 유효성 검사를 효율적으로 하도록 도와주는 라이브러리이다.

- 기존의 useState를 쓰면 input 개수만큼 useState()가 필요했다. 그래서 유효성 검사를 하기 위해선 if문이 늘어나 가독성이 낮아진다.
  <br>
  <br>

**그래서 장점은?**

- 리렌더링 줄여줌
- input에 register를 붙이면 RHF가 자동으로 값을 관리해줘서 코드가 깔끔해짐
- 다른 검증 라이브러리와 쉽게 결합이 가능함. 예를 들어 Zod, Yup, Joi등..

이중에서도 React Hook Form + Zod 조합을 가장 흔히 씀

```js
import { useForm } from 'react-hook-form';
import { z } from 'zod';
import { zodResolver } from '@hookform/resolvers/zod';

const schema = z.object({
  email: z.string().email('정확한 이메일 주소를 입력해주세요!'),
  name: z.string().min(2, '이름은 최소 2글자 이상 입력해주세요!'),
});
```
<br>

Date: 2025-09-29