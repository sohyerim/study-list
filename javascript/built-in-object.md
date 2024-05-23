# 빌트인 객체

- 빌트인 객체는 자바스크립트에서 이미 내장되어 있는 객체들을 말합니다.
- 이러한 객체들은 자바스크립트 실행 환경에 미리 정의되어 있어서 별도의 선언 없이 사용할 수 있습니다.
- 주로 데이터 구조, 수학 연산, 문자열 처리, 날짜 및 시간 관리 등 다양한 기능을 제공합니다.

### 1. Object
```javascript
// Object 빌트인 객체의 예제
const person = {
  name: 'John',
  age: 30,
  greet: function() {
    console.log(`Hello, my name is ${this.name} and I am ${this.age} years old.`);
  }
};
```
- Object 빌트인 객체는 자바스크립트에서 모든 객체의 조상입니다.
- 위 예제에서 person 객체는 name, age, greet 속성을 가지고 있습니다.
- 객체는 중괄호 {}로 표현되며, 속성들은 쉼표로 구분됩니다.
- 속성 값으로는 문자열, 숫자, 함수 등 어떤 값이든 올 수 있습니다.
- 함수 속성인 greet 메소드는 해당 객체의 정보를 출력하는 메시지를 로그에 출력합니다.
- 객체의 속성 및 메소드에는 점 표기법(object.property) 또는 대괄호 표기법(object['property'])을 사용하여 접근할 수 있습니다.

### 2. Array
```javascript
const fruits = ['apple', 'banana', 'orange'];

fruits.push('grape');

fruits.forEach(fruit => {
  console.log(fruit);
});
// 출력:
// apple
// banana
// orange
// grape

```
```javascript
const fruitsObject = {
  0: 'apple',
  1: 'banana',
  2: 'orange',
  length: 3,
  push: function(newFruit) {
    this[this.length] = newFruit;
    this.length++;
  }
};

fruitsObject.push('grape');

for (let i = 0; i < fruitsObject.length; i++) {
  console.log(fruitsObject[i]);
}
// 출력:
// apple
// banana
// orange
// grape
```

- Array 빌트인 객체는 순서가 있는 값들의 집합을 나타냅니다.
- 배열은 인덱스(index)를 사용하여 각 요소에 접근할 수 있으며, 인덱스는 0부터 시작합니다.
- 배열은 다양한 내장 메소드를 가지고 있어 요소 추가, 삭제, 변경, 검색 등 다양한 작업을 수행할 수 있습니다.
- 배열은 사실 객체입니다. 배열은 객체와 유사하게 키와 값을 가지고 있습니다.
- 배열은 특별한 속성인 length를 가지고 있습니다. 이 속성은 배열의 길이를 나타냅니다.
- 배열의 요소에 접근하기 위해 일반적으로 인덱스를 사용하지만, 실제로는 해당 인덱스를 키로 사용하여 값을 저장하고 있습니다.

### 3. String
```javascript
const message = 'Hello, world!';

console.log(message.length); // 출력: 13
console.log(message.toUpperCase()); // 출력: HELLO, WORLD!
console.log(message.includes('world')); // 출력: true
```
```javascript
const messageObject = {
  0: 'H',
  1: 'e',
  2: 'l',
  3: 'l',
  4: 'o',
  5: ',',
  6: ' ',
  7: 'w',
  8: 'o',
  9: 'r',
  10: 'l',
  11: 'd',
  length: 12,
  toUpperCase: function() {
    return this.split('').map(char => char.toUpperCase()).join('');
  },
  includes: function(substr) {
    return this.indexOf(substr) !== -1;
  }
};

console.log(messageObject.length); // 출력: 12
console.log(messageObject.toUpperCase()); // 출력: HELLO, WORLD!
console.log(messageObject.includes('world')); // 출력: true
```

- String 빌트인 객체는 텍스트 데이터를 나타냅니다.
- toUpperCase() 메소드는 문자열을 모두 대문자로 변환한 새로운 문자열을 반환합니다.
- includes() 메소드는 문자열에 특정 문자열이 포함되어 있는지 여부를 확인하고, 포함되어 있으면 true, 그렇지 않으면 false를 반환합니다.
- 문자열은 사실 문자들의 배열으로 생각할 수 있습니다. 각 문자는 문자열의 인덱스를 통해 접근할 수 있습니다.

### 4. Number
```javascript
const num = 42;

console.log(num.toString()); // 출력: "42"
console.log(num.toFixed(2)); // 출력: "42.00"
console.log(num.toPrecision(4)); // 출력: "42.00"
```
```javascript
const numObject = {
  value: 42,
  toString: function() {
    return this.value.toString();
  },
  toFixed: function(digits) {
    return this.value.toFixed(digits);
  },
  toPrecision: function(precision) {
    return this.value.toPrecision(precision);
  }
};

console.log(numObject.toString()); // 출력: "42"
console.log(numObject.toFixed(2)); // 출력: "42.00"
console.log(numObject.toPrecision(4)); // 출력: "42.00"
```

- Number 빌트인 객체는 숫자를 나타냅니다.
- toString() 메소드는 숫자를 문자열로 변환합니다.
- toFixed() 메소드는 소수점 이하 자릿수를 지정하여 문자열로 반환합니다.
- toPrecision() 메소드는 숫자의 전체 자릿수를 지정하여 문자열로 반환합니다.
-  숫자를 객체 형태로 표현하면 값으로 가지고 있는 value 속성과 다양한 메소드를 포함합니다.

### 5.Function

```javascript
function greet(name) {
  console.log(`Hello, ${name}!`);
}

const add = function(a, b) {
  return a + b;
};

console.log(typeof greet); // 출력: "function"
console.log(typeof add); // 출력: "function"
```
```javascript
const greetFunctionObject = {
  name: 'greet',
  length: 1,
  call: function(context, ...args) {
    return this(...args);
  }
};

console.log(typeof greetFunctionObject); // 출력: "object"
console.log(greetFunctionObject.length); // 출력: 1
greetFunctionObject.call(null, 'John'); // 출력: Hello, John!
```

- Function 빌트인 객체는 함수를 나타냅니다.
- 함수는 일급 객체로서, 변수에 할당하고 다른 함수의 매개변수로 전달할 수 있습니다.
- typeof 연산자를 사용하여 함수의 타입을 확인할 수 있습니다. 함수의 타입은 "function"입니다.
- 함수를 객체로 표현할 때, 주요 속성으로는 함수의 이름(name)과 매개변수의 개수(length)가 있습니다.
- 함수를 호출하는 call 메소드는 객체의 메소드로 정의되어 있습니다. 
- 이 메소드는 함수를 호출하며, 첫 번째 인자는 호출할 함수의 컨텍스트이며, 나머지 인자는 호출할 함수의 매개변수입니다.

### 6. Date
```javascript
const currentDate = new Date();

console.log(currentDate); // 현재 날짜와 시간을 출력
console.log(currentDate.getFullYear()); // 현재 연도를 출력
console.log(currentDate.getMonth()); // 현재 월을 출력 (0부터 시작)
console.log(currentDate.getDate()); // 현재 날짜를 출력
```
```javascript
const currentDateObject = {
  year: new Date().getFullYear(),
  month: new Date().getMonth() + 1,
  day: new Date().getDate(),
  getFormattedDate: function() {
    return `${this.year}-${this.month}-${this.day}`;
  }
};

console.log(currentDateObject.getFormattedDate()); // YYYY-MM-DD 형식의 현재 날짜를 출력

```

- Date 빌트인 객체는 날짜와 시간 정보를 다룹니다.
-  new Date()를 사용하여 현재 날짜와 시간 정보를 담은 Date 객체를 생성합니다.
- getFullYear() 메소드는 현재 연도를 반환합니다.
- getMonth() 메소드는 현재 월을 반환합니다. 단, 반환값은 0부터 시작하는 월을 나타냅니다. 즉, 1월은 0, 2월은 1, ..., 12월은 11입니다.
- getDate() 메소드는 현재 날짜를 반환합니다.
- 객체 내부에는 현재 연도, 월, 날짜를 저장하는 속성들이 있으며, 메소드인 getFormattedDate()를 통해 YYYY-MM-DD 형식으로 현재 날짜를 반환합니다.

### 7. Math
```javascript
console.log(Math.PI); // 원주율을 출력
console.log(Math.sqrt(16)); // 16의 제곱근을 출력
console.log(Math.floor(3.9)); // 3.9를 내림하여 출력
console.log(Math.random()); // 0과 1 사이의 난수를 출력
```
```javascript
const mathObject = {
  pi: Math.PI,
  squareRoot: function(x) {
    return Math.sqrt(x);
  },
  roundDown: function(x) {
    return Math.floor(x);
  },
  generateRandomNumber: function() {
    return Math.random();
  }
};

console.log(mathObject.squareRoot(16)); // 16의 제곱근을 출력
console.log(mathObject.generateRandomNumber()); // 0과 1 사이의 난수를 출력
```

- Math 빌트인 객체는 수학적인 연산을 제공합니다.
- Math.PI는 원주율을 나타내며, Math.sqrt()는 제곱근을 계산합니다.
- Math.floor()는 주어진 숫자를 내림하여 정수 부분을 반환합니다.
- Math.random()은 0과 1 사이의 난수를 반환합니다.
- 객체 내부에는 Math 객체의 메소드와 속성들이 포함되어 있습니다.