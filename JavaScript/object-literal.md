# 객체리터럴(object literal)이란 ?


### 객체 타입(object/reference type)
- 다양한 타입의 값(원시 값 또는 다른 객체)을 하나의 단위로 구성한 복합적인 자료구조이다.
- 객체 타입의 값은 변경 가능한 값(immutable value)이다.

## 구성
- 0개 이상의 프로퍼티로 구성되어 있으며, 프로퍼티는 키(key)와 값(value)으로 구성되어있다.
- 이때 JS에서 사용할 수 있는 모든 값은 프로퍼티 값이 될 수 있다.
- 특히 프로퍼티 값이 함수일 경우, 일반 함수와 구분하기 위해 메서드(method)라고 부른다.
- 프로퍼티와 메서드의 역할
    - 프로퍼티 : 객체의 상태를 나타내는 값(data)
    - 메서드 : 프로퍼티(상태 data)를 참조하고 조작할 수 있는 동작(behavior)

## 객체 리터럴
- JS는 프로토타입 기반 객체지향 언어로서, 다양한 객체 생성 방법을 지원한다.<br>(객체 리터럴, Object 생성자 함수, 생성자 함수, Object.create 메서드, 클래스)
- 이 방법들 중, 객체 리터럴은 가장 일반적이고 간단한 방법이다.
- 중괄호{} 내에 0개 이상의 프로퍼티를 정의한다.

## 프로퍼티 접근

```javascript
let babo = {
  name : "rootzero"
};

// 마침표 표기법
console.log(babo.name);  // "rootzero"
console.log(babo["name"]);  // "rootzero"
```
- 두 가지의 방법이 있다.
    - 마침표 표기법(dot notation) : 마침표 프로퍼티 접근 연산자(.)를 사용
    - 대괄호 표기법(bracket notation) : 대괄호 프로퍼티 접근 연산자([])를 사용
- 주의점
    - 대괄호 프로퍼티 접근 연산자 내부에 지정하는 프로퍼티 키는 반드시 따옴표로 감싼 문자열이어야 한다.
    - 객체에 존재하지 않는 프로퍼티에 접근하면 undefined를 반환한다.


## 프로퍼티 값 update
- 프로퍼티 동적 생성
```javascript
let babo = {
  name : "rootzero"
}

babo.age = 25;

console.log(babo);  // {name: "rootzero", age: 25}
```

- 프로퍼티 삭제
```javascript
let babo = {
  name : "rootzero"
}

babo.age = 25;

// delete 연산자로 age 프로퍼티를 삭제할 수 있다.
delete babo.age;

// babo에 address 프로퍼티가 존재하지 않는다.
// 이 때, 에러가 발생하지 않는다 !
delete babo.address; 

console.log(babo);  // {name : "rootzero"}
```
