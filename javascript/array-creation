# 배열 생성 방법

## 1. 배열 리터럴 표기법:
가장 일반적인 배열 생성 방법 중 하나입니다. 대괄호 `[]`를 사용하여 배열을 생성합니다.

```javascript
const fruits = ['사과', '바나나', '딸기'];
```

## 2. Array 생성자:
Array 생성자를 사용하여 배열을 생성할 수 있습니다.

```javascript
const numbers = new Array(1, 2, 3, 4, 5);
```

또는 배열의 길이만 지정하여 생성할 수도 있습니다.

```javascript
const emptyArray = new Array(5); // 길이가 5인 빈 배열 생성
```

## 3. 배열 전개 구문:
배열 전개 구문을 사용하여 다른 배열의 요소를 포함한 새 배열을 생성할 수 있습니다.

```javascript
const array1 = [1, 2, 3];
const array2 = [4, 5, 6];

const combinedArray = [...array1, ...array2]; // [1, 2, 3, 4, 5, 6]
```

## 4. Array.from():
Array.from() 메서드를 사용하여 유사 배열 객체나 이터러블 객체를 배열로 변환할 수 있습니다.

```javascript
const arrayLikeObject = {0: '사과', 1: '바나나', 2: '딸기', length: 3};
const array = Array.from(arrayLikeObject); // ['사과', '바나나', '딸기']
```

## 추가내용 - 유사배열객체
유사배열객체의 키값은 배열의 인덱스와 유사한 숫자 형태를 가지고 있고, length 속성을 가지고 있어 배열처럼 보이지만,
배열의 메서드와 속성을 직접적으로 사용할 수는 없다.
유사배열 객체를 배열로 변환하기 위해서는 Array.from()이나 배열 스프레드 구문을 사용해서 변환해 배열의 메서드와 속성을 사용한다.



## 5. Array.of():
Array.of() 메서드를 사용하여 전달된 인수를 요소로 가지는 배열을 생성할 수 있습니다.
```
const arrayWithValues = Array.of(1, 2, 3, 4, 5); // [1, 2, 3, 4, 5]
```