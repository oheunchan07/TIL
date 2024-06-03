# Quick Sort

## Quick Sort?
> 분할 정복 알고리즘 중 하나로 평균적으로 매우매우매우 빠르다.  
> 리스트 중에 피벗을 하나 설정한다.  
> 피벗을 기준으로 피벗보다 작은 원소들은 모두 피벗의 왼쪽으로 옮겨지고 피벗보다 큰 요소들은 모두 피벗의 오른쪽으로 옮겨진다.  
> 피벗을 제외한 왼쪽 리스트와 오른쪽 리스트를 다시 정렬한다.  
> 리스트가 0또는 1이 될 때 까지 반복한다.

![image](https://github.com/oheunchan07/TIL/assets/131967057/5533cc56-102b-4375-8a65-e29c2b871c87)


## Quick Sort 장단점
### 장점
* 개빠르다.
* 추가적으로 메모리 공간이 필요없다.  

### 단점
* 만들기 어렵다.

## Quick Sort 시간 복잡도
> 최선, 평균: T(n) = O(n log2 n)
> 최악: T(n) = O(n^2)

## Quick Sort 코드
``` java
public class QuickSort {
    public static void sort(int[] a) {
        l_pivot_sort(a, 0, a.length - 1);
    }

    private static void l_pivot_sort(int[] a, int lo, int hi) {

        if(lo >= hi) {
            return;
        }
        int pivot = partition(a, lo, hi);	

        l_pivot_sort(a, lo, pivot - 1);
        l_pivot_sort(a, pivot + 1, hi);
    }

    private static int partition(int[] a, int left, int right) {

        int lo = left;
        int hi = right;
        int pivot = a[left];

        while(lo < hi) {
            
            while(a[hi] > pivot && lo < hi) {
                hi--;
            }
			
            while(a[lo] <= pivot && lo < hi) {
                lo++;
            }
			
            swap(a, lo, hi);
        }
        swap(a, left, lo);
        return lo;
    }

    private static void swap(int[] a, int i, int j) {
        int temp = a[i];
        a[i] = a[j];
        a[j] = temp;
    }
}
```