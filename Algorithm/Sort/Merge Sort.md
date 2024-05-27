# Merge Sort

## Merge Sort?
> 합병 정렬은 안정적인 정렬에 속하며, 분할 정복 알고리즘 중 하나다.  
> 하나의 리스트를 두 개의 균등한 크기로 분할하고 분할된 리스트들을 정렬한 다음에 두 개의 정렬된 리스트들을 합하여 전체가 정렬된 리스트가 되게 하는 방법이다.

![image](https://github.com/oheunchan07/TIL/assets/131967057/6ebbc62b-3dc2-44b1-a3b0-6dcfea1bff77)


## Merge Sort 장단점
### 장점
* 빠르다
* 입력데이터가 뭐든 간에 정렬되는 시간은 같다.

### 단점
* 배열로 구성한다면 임시 배열이 필요하다.
* 레코드가 크기가 큰 경우에는 이동 횟수들이 많아 크게 시간낭비를 한다.

## Merge Sort 시간 복잡도
> 최선, 최악, 평균이 모두 같다.  
> T(n) = O(n log2 n)

## Merge Sort 코드
```
private static void merge(int[] a, int left, int mid, int right) {
    int l = left;
    int r = mid + 1; 
    int idx = left;	

    while(l <= mid && r <= right) {
        if(a[l] <= a[r]) {
            sorted[idx] = a[l];
            idx++;
            l++;
        }
        else {
            sorted[idx] = a[r];
            idx++;
            r++;
        }
    }

    if(l > mid) {
        while(r <= right) {
            sorted[idx] = a[r];
            idx++;
            r++;
        }
    }	    
    else {
        while(l <= mid) {
            sorted[idx] = a[l];
            idx++;
            l++;
        }   
    }
    for(int i = left; i <= right; i++) {
        a[i] = sorted[i];
    }   
}
```