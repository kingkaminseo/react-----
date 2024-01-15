React 기초 개념
React는 페이스북에서 개발한 JavaScript 라이브러리로, 사용자 인터페이스를 만들기 위한 도구이다. React를 사용하면 UI를 구성하는 데 있어서 선언적이고 효율적인 방법으로 작성할 수 있다.
(코드 재사용가능, 유지보수 원활)

1. 컴포넌트 (Components)
리액트는 화면에서 UI 요소를 구분할 때 '컴포넌트'라는 단위를 사용한다.
컴포넌트 에는 함수 컴포넌트, 클래스 컴포넌트 2가지가 있습니다.
(ex : 레고 블록으로 집을 쌓게 된 경우 하나의 블록이 컴포넌트 라고 할 수 있다.)


## 예시코드 (함수형 컴포넌트)
```jsx
function MyComponent() {
  return <div>Hello, World!</div>;
}
```


3. State와 Props
State (상태)
State는 컴포넌트의 상태를 관리하는 데 사용됩니다. 상태가 변경되면 React는 자동으로 화면을 업데이트한다.

```jsx
import React, { useState } from 'react';

function Counter() {
  const [count, setCount] = useState(0);

  return (
    <div>
      <p>Count: {count}</p>
      <button onClick={() => setCount(count + 1)}>Increment</button>
    </div>
  );
}
```

setState()는 컴포넌트의 state 객체에 대한 업데이트를 실행합니다. state가 변경되면, 컴포넌트는 리렌더링된다.



### state
Props (속성)
Props는 부모 컴포넌트에서 자식 컴포넌트로 데이터를 전달하는 데 사용한다.

~~~jsx
// 예시: Props 사용
function Greet(props) {
  return <p>Hello, {props.name}!</p>;
}
~~~

### state와 props의 차이점

props (“properties”의 줄임말) 와 state 는 일반 JavaScript 객체입니다. 두 객체 모두 렌더링 결과물에 영향을 주는 정보를 갖고 있는데, 한 가지 중요한 방식에서 차이가 있다. props는 (함수 매개변수처럼) 컴포넌트에 전달되는 반면 state는 (함수 내에 선언된 변수처럼) 컴포넌트 안에서 관리된다.



4. 이벤트 처리
React에서 이벤트는 적절한 이벤트 핸들러 함수와 함께 JSX에 직접 포함됩니다.

~~~jsx
Copy code
// 예시: 이벤트 처리
function ClickHandler() {
  const handleClick = () => {
    console.log('Button clicked!');
  };

  return <button onClick={handleClick}>Click me</button>;
}
~~~
5. 라이프사이클 메서드
라이프사이클 메서드는 컴포넌트가 생성, 업데이트, 소멸될 때 일어나는 특정한 단계에 실행되는 메서드이다. (※ React 16.3 이후 버전부터는 클래스형 컴포넌트에서 사용이 권장되지 않으며, 대신 Hooks를 사용하도록 권장된다.)

6. Hooks
Hooks는 함수형 컴포넌트에서 상태(state)와 생명주기 메서드를 사용할 수 있게 해주는 기능이다. 주로 useState, useEffect, useContext 등을 다룬다.

