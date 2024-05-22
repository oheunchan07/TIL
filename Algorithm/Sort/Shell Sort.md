# Shell Sort

## Shell Sort?
> 삽입 정렬을 보안한 알고리즘이다.  
> 정렬해야 할 리스트의 각 k번째 원소를 추출해서 부분 리스트를 만든다.  
> 한 바퀴 회전할 때 마다 k를 절반으로 나눈다.  
> k가 1이 될때까지 반복한다.  

![image](https://github.com/oheunchan07/TIL/assets/131967057/7e0ee554-ec91-4d78-aae4-04b24b277c9c)

## Shell Sort 장단점
### 장점
* 연속적이지 않은 부분 리스트에서 자료의 교환이 일어나면 더 큰 거리를 이동한다.
* 삽입 정렬보다 빠르다.
* 구현하기 간단하다.

### 단점
* 간격이 잘못되면 성능히 굉장히 떨어진다.

## Shell Sort 시간 복잡도
> 최선: T(n) = O(n)
> 평균: T(n) = O(n^1.5)
> 최악: T(n) = O(n^2)

## Shell Sort 코드
```
public class Shell_Sort {

    private final static int[] gap = 
        { 1, 4, 10, 23, 57, 132, 301, 701, 1750, 3937, 	
        8858, 19930, 44842, 100894, 227011, 510774,
        1149241, 2585792, 5818032, 13090572, 29453787, 
        66271020, 149109795, 335497038, 754868335, 1698453753}; 

    public static void shell_sort(int[] a) {
        shell_sort(a, a.length);    
    }

    private static int getGap(int length) {
        int index = 0;
        int len = (int)(length / 2.25);	
        while (gap[index] < len) {
            index++;
        }
        return index;
    }
	
    private static void shell_sort(int[] a, int size) {
        int gapIndex = getGap(size);

        while(gapIndex >= 0) {
            int step = gap[gapIndex--];

            for(int i = step; i < size; i++) {
                for (int j = i; j >= step && a[j] < a[j - step]; j -= step) {
                    swap(a, j, j - step);
                }
            }
        }   
    }
 
    private static void swap(int[] a, int i, int j) {
        int swap = a[i];
        a[i] = a[j];
        a[j] = swap;
    }
}
```