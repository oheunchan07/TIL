# Insertion Sort

## Insertion Sort?
> 리스트의 모든 원소들을 앞에서부터 차례대로 이미 정렬이 되있는 리스트 부분과 비교하며 자신의 위치에 삽입하는 알고리즘이다.  
> 두 번째 원소부터 시작하여 그 앞의 원소들과 비교하여 삽입할 위치를 지정한 후 자료를 뒤로 옮기고 지정한 자리에 원소를 삽입하여 정렬하는 알고리즘이다.

![image](https://github.com/oheunchan07/TIL/assets/131967057/718bddac-a79b-43a9-bab8-8d7c447bc9ef)

## Insertion Sort 장단점
### 장점
* 리스트가 거의 다 정렬이 되어있다면 매우 빠르다.
* 리스트 안에 원소 개수가 적을 경우에는 알고리즘 이 간단해 다른 정렬보다 효율적이다.  

### 단점
* 리스트 안에 원소 수가 많다면 비효율 적이다.

## Insertion Sort 시간 복잡도
> 최선: T(n) = O(n)
> 최악, 평균: T(n) = O(n^2)

## Insertion Sort 코드
``` java
public class Insertion_Sort {
    public static void insertion_sort(int[] a) {
        insertion_sort(a, a.length);
    }

    private static void insertion_sort(int[] a, int size) {		
        for(int i = 1; i < size; i++) {
            int target = a[i];			
            int j = i - 1;

            while(j >= 0 && target < a[j]) {
                a[j + 1] = a[j];
                j--;
            }

            a[j + 1] = target;	
        }
    }
}
```