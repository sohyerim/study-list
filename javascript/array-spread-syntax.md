# 배열 스프레드 문법

배열을 펼쳐서 새로운 배열을 반환하는 문법으로 기존 배열은 변경되지 않고 복사된 배열을 반환한다.

### 두 배열 합치기:

```javascript
const arr1 = [1, 2, 3];
const arr2 = [4, 5, 6];
const combinedArray = [...arr1, ...arr2]; // [1, 2, 3, 4, 5, 6]
```

### 특정 위치에 요소 삽입:

``` javascript
코드 복사
const originalArray = [1, 2, 4, 5];
const newArray = [...originalArray.slice(0, 2), 3, ...originalArray.slice(2)]; // [1, 2, 3, 4, 5]
```

### 특정 인덱스 요소 삭제:

```javascript
코드 복사
const originalArray = [1, 2, 3, 4, 5];
const newArray = [...originalArray.slice(0, 2), ...originalArray.slice(3)]; // [1, 2, 4, 5]
```

### 배열 요소 업데이트:

```javascript
코드 복사
const originalArray = [{ id: 1, value: 'A' }, { id: 2, value: 'B' }, { id: 3, value: 'C' }];
const updatedArray = originalArray.map(item => item.id === 2 ? { ...item, value: 'D' } : item);
// [{ id: 1, value: 'A' }, { id: 2, value: 'D' }, { id: 3, value: 'C' }]
```