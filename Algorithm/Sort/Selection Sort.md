# Selection Sort

## Selection Sort?
> 해당 순서에 원소를 넣을 위치는 이미 정해져 있고, 어떤 원소를 넣을지 선택하는 알고리즘이다.  
> 선택 정렬은 첫 번째 원소부터 마지막 원소까지 차례대로 비교하여 가장 작은 값을
앞에 두는 것을 반복한다.  
> 회전을 수행하고 나면 가장 작은 값의 자료가 맨 앞에 오게 되므로 그 다음 회전에서는 두 번째 자료를 가지고 비교한다.

![image](https://github.com/oheunchan07/TIL/assets/131967057/dad395cf-9d60-4404-a50e-d25c7b327e96)

## Selection Sort 장단점
### 장점
* 원소의 이동회수가 정해져 있다.
* 구현하기 쉽다.

### 단점
* 안정성을 만족하지 않는다
  * 같은 값이 리스트에 있다면 상대적으로 위치가 변경 될 수 있다.
* 시간이 버블 정렬 다음으로 오래 걸린다.

## Selection Sort 시간 복잡도
> 최선, 최악, 평균이 모두 같다.  
> T(n) = O(n^2)

## Selection Sort 코드
```
public static void selection_sort(int[] a, int size) {
	for(int i = 0; i < size - 1; i++) {
        int min_index = i;	
        for(int j = i + 1; j < size; j++) {
            if(a[j] < a[min_index]) {
                min_index = j;
            }
        }
        int temp = a[i];
        a[i] = a[j];
        a[j] = temp;
    }
}
```