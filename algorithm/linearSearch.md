# 선형검색
리스트 안의 특정 데이터를 찾기 위해 리스트의 앞쪽에서부터 데이터를 하나 확인하는 방법.

정렬되지 않은 리스트에서 유용하다.

## 구현코드
```js
function linearSearch(arr, n){
    for(let i = 0; i < arr.length; i++) {
        if(arr[i] === n) return i; // true
    }
    
    return -1; // false
}
```

## Big O 복잡도
최선 : O(1)

최악 : O(n)

평균 : O(n)
