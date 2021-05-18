---
layout: post
title: "JS: 변수와 자료형"
tags: Javascript
---

JavaScript가 제공하는 자료형은 
>`undefined`, `null`, `boolean`, `string`, `symbol`, `bigint`, `number`, `object`

## 변수
`Variables`를 사용하여 컴퓨터는 데이터를 동적 방식으로 저장하고 조작한다. 이 경우, 데이터 자체를 사용하지 않고 `label`을 사용하여 데이터를 가리킨다.
```javascript
let foo; // foo라는 변수를 만든다.
foo = 5; /* foo에 5를 할당한다. 
 foo가 코드에 다시 나타면 프로그램은 foo를 5인 것처럼 처리한다. */
```
`= operator` 오른쪽에 계산이 있는 경우에는 값이 operator 연산자 왼쪽의 변수에 할당되기 전에 계산이 수행된다.
```javascript
let foo;
foo = 5;
let bar;
bar = foo; // bar 변수에 foo의 값이 할당된다.
```
## Uninitialized Variables
```javascript
let a;
let b = 1;
console.log(a+b); // NaN(Not a Number)이 출력된다.
```
## camelCase
변수명은 `camelCase`로 작성한다.
```javascript
let thisVariableNameIsSoLong;
```
## 상수
```javascript
const a = 1;
```
값을 한 번 선언하면 바뀌지 않는다. 값이 고정적이다. 
## 문자열
`string`값을 선언할 때에는 큰따옴표, 혹은 작은 따옴표로 엮어서 선언한다. (velopert님은 작은 따옴표를 선호한다고 한다.)
```javascript
let foo = "not shy";
```
## Escaping Literal Quotes
* `string` 내부에 `""`나 `''`가 있다면?
```javascript
let dallaDallaLyrics = "you better check yourself, \"말리지마!\"";
```

## var
변수를 선언하는 또 하나의 방법은 var라는 키워드를 쓰는건데, 모던 자바스크립트에서는 사용하지 않기 때문에 그냥 잊어버리는 것이 낫다.

선언되었는지를 check하는 `let`이나 `const`와는 다르게 이전에 선언된 변수가 존재하고 있더라도 덮어써버리고 오류를 발생시키지 않기 때문에, `var`를 통한 선언은 상대적으로 안전하지 못한 방법일 수 있다.

## null과 undefined
```javascript
const friend = null; // 값이 없다! 라고 선언해주는 것
let job;
console.log(job); /* job이라는 변수는 선언되었지만
값이 지정되지 않았기 때문에 undefined가 반환된다. */
```
