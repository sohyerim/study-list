# 🌟 배열의 고차함수

- 매개변수로 콜백함수가 들어가는 경우가 많다.
- 배열을 순회하는 경우가 많다.
- 배열의 유틸 기능이 많다.

1. map
    - 배열을 순회한다. (순서대로 반복)
    - 반복 시마다 각 요소에 콜백함수의 반환 값을 요소로 하는 새로운 배열을 생성한다.
    - 새로운 배열의 필요에 의해 사용한다. (반복문처럼 사용하면 안 된다.)
    - 콜백함수의 두 번째 인자로는 인덱스가 들어간다.
    
    ```jsx
    const posts = [
    	{
    		id: 1,
    		title: "안녕하세요"
    	},
    	{
    		id: 2,
    		title: "반갑습니다"
    	}
    ];
    // 배열 ["<div>안녕하세요</div>", "<div>반갑습니다</div>"] 만들기
    ```
    
    ```jsx
    // 일반 반복문
    
    let postHtml = [];
    for (let i = 0; i < posts.length; i++) {
    	postHtml.push(`<div>${posts[i].title}</div>`);
    };
    console.log(postHtml);
    ```
    
    ```jsx
    // map 사용
    
    let postHtml = [];
    postHtml = posts.map((post) => `<div>${post.title}</div>`);
    console.log(postHtml);
    ```
    

1. filter
    - 배열에서 내가 원하는 요소들만 찾아서 새로운 배열을 반환한다.
    - 특정한 조건에 맞는 배열이나 특정한 값을 삭제한 배열이 필요할 때 사용한다.
    - 조건이 true일 때, 해당 요소를 배열로 반환한다.
    
    ```jsx
    const userList = [
            {
              name: "소혜림",
              age: 32,
              height: 162
            },
            {
              name: "이강인",
              age: 23,
              height: 173
            },
            {
              name: "홍길동",
              age: 18,
              height: 180
            }
          ];
    
    // 성인인 user만 배열로 반환하기
    
    const filterUserList = userList.filter((user) => user.age > 20);
    
    console.log(filterUserList);
    
    // result
    // [{name: "소혜림", age: 32, height: 162}, {name: "이강인", age: 23, height: 173}]
    ```
    
    - filter는 특정 값을 삭제하고 싶을 때도 사용하는데, splice와의 차이는 splice는 원본 배열의 값을 삭제하지만 filter는 원본 배열의 값을 삭제하지 않고 새로운 복사본을 생성한다는 점이 다르다.
    
    ```jsx
    const userList = [
            {
              name: "소혜림",
              age: 32,
              height: 162
            },
            {
              name: "이강인",
              age: 23,
              height: 173
            },
            {
              name: "홍길동",
              age: 18,
              height: 180
            }
          ];
          
     let deleteUserList = userList.filter((user) => user.name !== "홍길동");
     console.log(deleteUserList);
     
     // result (홍길동 user를 삭제한 배열 출력)
     // [{name: "소혜림", age: 32, height: 162}, {name: "이강인", age: 23, height: 173}]
    ```
    

1. find
    - 배열에서 특정한 조건을 만족하는 요소를 찾아서 반환한다.
    - 배열이 아닌 요소를 반환한다. 🌟
    - 배열을 순회하며,  조건식에 맞는 가장 첫번째 요소를 반환한다. (만약 가장 마지막 요소를 반환하고 싶을 때는 reverse를 사용하면 된다.)
    - 배열에서 특정한 객체를 찾을 때는 같은 내용의 객체라고 하더라도 주소를 비교할 수 없기 때문에 includes로 찾기가 어려워 대신 find와 findIndex와 같이 배열을 순회하는 함수를 사용한다. 🌟
    
2. findIndex
    - find와 모든 원리가 같지만 요소 대신 index를 반환한다.
    - 값이 없다면 -1을 반환한다.

1. reduce
    - 배열을 순회하며 연산의 결과를 누적시켜 반환한다.
    - 첫번째 순회 시 누적값의 초기값은 첫번째 요소이고, 현재요소는 두번째 요소다.
    - 단, reduce의 두번째 인자에 누적값의 기본값을 설정할 수 있는데, 이 경우 첫번째 요소는 기본값이 되고, 두번째 요소는 배열의 첫번째 값이 온다.
    - 배열의 모든 요소를 순회하면서 누적되는 값이 있을 경우 reduce를 쓰는 것을 고민한다.
    - 다음 연산에 이전까지의 연산이 필요할 때 reduce를 쓰는 것을 고민한다.
    
    ```jsx
    // 배열.reduce((누적값, 현재요소, 인덱스) ⇒ {return 연산 }, 기본값);
    
    const numArr = [1, 2, 3, 4, 5]
    numArr.reduce((sum, n) => {
    	return sum + n
    }, 0);
    
    // 현재 요소와 다음 요소를 더하여 누적시켜 나간다.
    // 15
    ```
    
2. every
    - 배열에서 모든 요소의 조건이 참인지 확인한다.
    - 특정 조건이 모두 만족하느냐에 따라서 분기처리를 할 수 있다.
    
    ```jsx
    const arr = [2, 4, 6, 8]
    
    arr.every((el) => el%2 === 0);
    
    // true
    ```
    
3. some
    - 배열에서 하나 이상의 요소가 참인지 확인하는 것이다.
    
    ```jsx
    const arr = [2, 4, 5, 8, 7]
    arr.some((el) => el%2 === 1) // 5, 7 => true
    ```
    
4. sort
    - 원본 배열의 요소를 크기대로 정렬한다.
    - 유니코드 순으로 정렬을 한다.
    
    ```jsx
    const arr = [5, 3, 1, 2, 4]
    arr.sort() // 1, 2, 3, 4, 5
    ```