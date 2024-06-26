# 반복문 예제:

## for 문:

- for 문은 초기화식, 조건식, 증감식으로 구성되어 있습니다.
- 초기화식은 반복문이 시작하기 전에 단 한 번 실행됩니다.
- 조건식은 반복문이 실행될 조건을 지정합니다. 조건식이 참(true)이면 반복문이 실행됩니다.
- 증감식은 각 반복 후에 실행되며, 보통 변수를 증가시키거나 감소시키는 역할을 합니다.

```javascript
// for (초기화식; 조건식; 증감식) {
//   실행코드
// }

for (let i = 0; i < 5; i++) {
    console.log(i); // 0, 1, 2, 3, 4
}
```

## while 문:

- while 문은 조건식이 참(true)인 동안 코드 블록을 반복적으로 실행합니다.
- 코드 블록을 실행하기 전에 조건식을 검사하므로, 조건식이 false가 되면 코드 블록은 실행되지 않습니다.

```javascript
// while (조건식) {
//  실행코드
//  증감식
// }

let i = 0;
while (i < 5) {
    console.log(i); // 0, 1, 2, 3, 4
    i++; 
}
```

## do...while 문:

- do...while 문은 while 문과 비슷하지만, 코드 블록을 먼저 실행한 다음에 조건식을 검사합니다.
- 따라서 코드 블록은 최소 한 번은 실행되며, 조건식이 false가 되더라도 코드 블록은 최소 한 번은 실행됩니다.

```javascript
// do {
//   실행코드
//   증감식
// } while (조건식);

let i = 0;
do {
    console.log(i); // 0, 1, 2, 3, 4
    i++;
} while (i < 5);
```

## for...of 문 (배열 순회용):

- for...of 문은 배열의 각 요소를 순회할 때 사용됩니다.
- 배열의 요소를 순서대로 가져와서 반복문의 코드 블록을 실행합니다.

```javascript

// for (변수 of 배열) {
//   배열을 순회하며 실행할 코드
// }

const arr = [1, 2, 3];
for (let value of arr) {
    console.log(value); // 1, 2, 3
}
```

## for...in 문 (객체 순회용):

- for...in 문은 객체의 속성을 열거할 때 사용됩니다.
- 객체의 속성을 열거하여 반복문의 코드 블록을 실행합니다.

```javascript

// for (key가 저장되는 변수 in 객체) {
//   실행코드(객체 키 사용)
// }

const obj = { a: 1, b: 2, c: 3 };
for (let key in obj) {
    console.log(key, obj[key]); // a 1, b 2, c 3
}
```

## forEach 메서드

- 배열의 각 요소에 대해 지정된 함수를 실행합니다.

```javascript
// 배열.forEach(function(요소, 인덱스) {
//     // 코드 블록
// });
const fruits = ['사과', '바나나', '딸기', '포도'];

// 배열의 각 요소에 대해 작업하는 forEach 메서드를 호출합니다.
fruits.forEach(fruit => {
    console.log(fruit);
}); //사과 바나나 딸기 포도
```