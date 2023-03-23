# 이진검색
선형검색과는 다르게 __정렬된__ 리스트에서만 사용가능함

이진검색은 중간값을 기준으로 찾는 값이 중간값보다 큰지, 작은지를 따지며 검색범위를 절반씩 줄여나갈 수 있기 때문에

빠르게 검색이 가능한 장점이 있다

## 구현코드
```js
function binarySearch(arr, n) {
    let start = 0;
    let end = arr.length - 1;
    let mid = ~~((start + end) / 2);

    while(start <= end) {
        if(arr[mid] === n) return mid;
        if(arr[mid] > n) end = mid - 1;
        if(arr[mid] < n) start = mid + 1;

        mid = ~~((start + end) / 2);
    }

    return -1;
}
```

## Big O 복잡도
최선 : O(1)

최악 : O(log n)

평균 : O(log n)
