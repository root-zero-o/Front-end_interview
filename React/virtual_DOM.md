# virtual DOM 이란?

- 리액트는 virtual DOM 방식을 사용해 DOM 업데이트를 ```추상화```함으로써 DOM 처리 횟수를 최소화하고 효율적으로 진행한다.
- 실제 DOM에 접근하여 조작하는 대신, 이를 ```추상화```한 자바스크립트 객체를 구성해 사용
- 리액트에서의 DOM 업데이트 절차 <br><br>
    >1. 데이터를 업데이트하면 전체 UI를 virtual DOM에 리렌더링한다.
    >2. 이전 virtual DOM에 있던 내용과 현재 내용을 비교한다.
    >3. 바뀐 부분만 실제 DOM에 적용한다.
- 이러한 접근방식이 리액트의 선언적 API를 가능하게 한다.

## 참고
- 리액트를 다루는 기술
- https://ko.reactjs.org/docs/faq-internals.html
