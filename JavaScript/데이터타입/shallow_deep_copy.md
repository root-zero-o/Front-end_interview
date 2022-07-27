# 얕은 복사 & 깊은 복사

- 객체의 경우 얕은 복사는 한 단계까지만 복사하는 것을 말하고, 깊은 복사는 객체에 중첩되어 있는 객체까지 모두 복사하는 것을 말한다.

```javascript
const o = { x : { y : 1 }};

// 얕은 복사
const c1 = {...o};
console.log(c1 === o);  // false
console.log(c1.x === o.x)  // true

// 깊은 복사(lodash 이용)
const _ = require("lodash");
const c2 = _.cloneDeep(o);
console.log(c2 === o);  // false
console.log(c2.x === o.x);  // false
```
- 얕은 복사와 깊은 복사로 생성된 객체는 ```원본과는 다른 객체```이다.
- ```얕은 복사```는 객체에 중첩되어 있는 객체의 경우 참조값을 복사하고, ```깊은 복사```는 객체에 중첩되어 있는 객체까지 모두 복사해서 원시값처럼 완전한 복사본을 만든다.

----

**```원시값```을 할당한 변수를 다른 변수에 할당하는 것을 ```깊은 복사```, ```객체```를 할당한 변수를 다른 변수에 할당하는 것을 ```얕은 복사```라고 부르는 경우도 있다.*

```javascript
const v = 1;

// 깊은 복사
const c1 = v;
console.log(c1);  // true

const o = { x : 1 };

// 얕은 복사
const c2 = o;
console.log(c2 === o);
```

## 참고
- 모던 자바스크립트 Deep Dive(이웅모 저)
