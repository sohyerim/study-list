# 🌟배열의 내장함수

- 함수별로 함수의 기능과 복사본의 유무 그리고 반환 값이 무엇인지가 중요하다.

1. push()
    - ()안의 데이터를 원본 배열의 맨 끝 요소로 추가한다.
    
    ```jsx
    arr = ["이강인", "손흥민"]
    arr.push("황희찬")
    console.log(arr)
    ```
    
    ```jsx
    이강인 손흥민 황희찬
    ```
    
2. pop()
    - 원본 배열의 맨 끝 요소를 제거, 제거된 요소를 반환한다.
    
    ```jsx
    arr = ["이강인", "손흥민", "황희찬"]
    let el = arr.pop()
    console.log(arr)
    ```
    
    ```jsx
    이강인 황희찬
    ```
    
    ```jsx
    console.log(el)
    ```
    
    ```jsx
    황희찬
    ```
    
3. unshift()
    - ()안의 데이터를 원본 배열의 맨 앞에 추가한다.
    
    ```jsx
    const arr = [1, 2, 3, 4]
    arr.unshift(0)
    console.log(arr)
    ```
    
    ```jsx
    0 1 2 3 4
    ```
    
4. shift()
    - 원본 배열의 맨 앞 요소를 제거, 제거된 요소를 반환한다.
    
    ```jsx
    const arr = [0, 1, 2, 3, 4]
    let el = arr.shift()
    console.log(arr)
    ```
    
    ```jsx
    1 2 3 4
    ```
    
    ```jsx
    console.log(el)
    ```
    
    ```jsx
    0
    ```
    
5. 배열1.concat(배열2)
    - 배열1과 ()안의 또 다른 배열2를 합친 하나의 복사본 배열을 반환한다.
    
    ```jsx
    const arr1 = [1, 2, 3, 4]
    const arr2 = [5, 6, 7, 8]
    
    let concat = arr1.concat(arr2)
    console.log(arr1)
    ```
    
    ```jsx
    1 2 3 4
    ```
    
    ```jsx
    console.log(concat)
    ```
    
    ```jsx
    1 2 3 4 5 6 7 8
    ```
    
    🌟 원본 배열은 변하지 않고, 복사본을 반환한다.
    
6. join()
    - 배열 사이에 ()안의 원하는 문자가 삽입된 문자열을 반환
    - 주로 배열을 문자열로 반환하고 싶을 때 사용한다.
    
    ```jsx
    const ph = ["010", "1234", "1234]
    const strPh = ph.join("-")
    console.log(strPh)
    ```
    
    ```jsx
    “010-1234-1234”
    ```
    

1. reverse()
    - 원본 배열을 역순으로 배치를 한다.
    
    ```jsx
    const arr = [1, 2, 3, 4]
    arr.reverse()
    console.log(arr)
    ```
    
    ```jsx
    4 3 2 1
    ```
    

1. split()
    - 문자열을 ()안의 문자를 기준으로 배열로 생성
    
    ```jsx
    const str = "안녕하세요"
    str.split()
    console.log(str)
    ```
    
    ```jsx
    안 녕 하 세 요
    ```
    
    ```jsx
    const ph = "010-1234-1234"
    ph.split("-")
    console.log(ph)
    ```
    
    ```jsx
    010 1234 1234
    ```
    
2. splice(start, count, item)
    - 원본 배열의 요소를 제거하고,
    - 제거한 부분에 item으로 대체한다. (복수 가능)
    - start(index), count(제거할 개수)
        
        ```jsx
        const arr = [1, 2, 3, 4, 5, 6, 7]
        arr.splice(3, 3, "hello")
        // 인덱스 3번째부터 시작해서 3개를 지우고 hello로 대체한다.
        console.log(arr)
        ```
        
        ```jsx
        1 2 3 hello 7
        ```
        
    
3. slice(start, end)
    - 원본 배열의 특정 구간을 잘라서 복사본으로 생성한다.
    - splice와 달리 제거하지 않는다.
    - start부터 시작해서 end 직전의 index까지를 범위로 한다.
    
    ```jsx
    const arr = [1, 2, 3, 4, 5, 6, 7]
    // 4, 5, 6을 복사본으로 생성하기
    let a = arr.slice(3, 6)
    console.log(a)
    ```
    
    ```jsx
    4, 5, 6
    ```
    
4. indexOf
    - 배엻에 특정한 값의 인덱스를 찾기 위해 사용한다.
    - 찾는 값이 없는 경우 -1을 반환한다.
    - 이 배열에 해당 값이 포함되어있는지 확인하기 위해 쓰였으나, 현재는 includes를 많이 사용한다.
    - 내가 찾고자 하는 요소의 index가 필요할 때 사용한다.
    
    ```jsx
    const arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
    let idx = arr.indexOf(7)
    console.log(idx)
    ```
    
    ```jsx
    6
    ```
    

1. includes
    - 특정 값이 포함되어 있는지를 확인하여 true와 false를 반환한다.
    
    ```jsx
    const arr = [1, 2, 3, 4, 5, 6, 7]
    let bool = arr.includes(7)
    console.log(bool)
    ```
    
    ```jsx
    true
    ```