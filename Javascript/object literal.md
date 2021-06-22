# 객체 리터럴

## 01. 객체의 속성값에 접근하는 방법 obj.속성이름

```javascript
const abc = {
  name: "aaa",
  year: 1111,
  month: 11,
  date: 11,
  gender: "F",
};
console.log(abc.name);
console.log(abc["name"]);
```

#### 특수한 속성이름(특수문자, 띄어쓰기) 경우 속성값에 접근하는 방법 obj['속성이름']

```javascript
const obj = {
  bc: "hello",
  "2ca": "hello1",
  "c a": "hello2",
  "c - a": "hello3",
};
console.log(obj.bc); //hello
console.log(obj["bc"]); //hello
console.log(obj.c - a); //error
console.log(obj["c - a"]); //hello3, 특수한 경우
```

## 02. 객체 속성 수정 하기

```javascript
const abc = {
  name: "aaa",
  year: 1111,
  month: 11,
  date: 11,
  gender: "F",
};
abc.gender = "M";
console.log(abc.gender);
<결과>
M
```

## 03. 객체 속성 제거 하기

```javascript
const abc = {
  name: "aaa",
  year: 1111,
  month: 11,
  date: 11,
  gender: "F",
};
delete abc.gender;
console.log(abc.gender);
<결과>
값이 없어서 undefined
```

## 04. 메서드 이해하기 객체안에 속성값으로 함수를 넣었을때 이 속성을 메서드라고 함.

```javascript
const debug = {
  log: function (value) { //method
    console.log(value);
  },
};
debug.log("hello");
<결과>
hello
```

## 05. 객체간의 비교,

#### {} === {} => false

```javascript
const debug = {
  log: function (value) {
    console.log(value);
  },
};
const bug = {
  log: function (value) {
    console.log(value);
  },
};
console.log(debug === bug);
<결과>
false
```

#### object 비교하려면 기존 객체를 변수에 저장하고 비교

```javascript
const a = { name: "holim" };
const arr = [1, 2, a];
console.log(a === arr[2]);
<결과>
true
```

## 06. 참조와 복사

```javascript
const a = { name: "holim" };
const b = a;
a.name = "hero";
console.log(b.name);
console.log(a === b);
<결과>
hero
true
```

#### 객체가 아닌값(문자열, 숫자, bool, null, undefined)

```javascript
let a = "holim";
let b = a;
a = "hero";
console.log(a === b);
<결과>
false
```

## 문제 'L' 값에 접근 하는 방법은?

```javascript
const holimL = {
  name: {
    first: "holim",
    last: "L",
  },
  gender: "m",
};

<답>
holimL.name.last;
holimL["name"]["last"];
```
