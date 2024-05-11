# Bubble Sort

## Bubble Sort?
> 서로 인접한 두 원소를 검사하여 정령하는 알고리즘이다.  
> 2개의 원소씩 검사하여 크기가 순서대로 되어 있지 않는다면 교환한다.  
> 1회전을 수행하면 가장 큰 원소가 맨뒤로 이동된다.

![image](https://github.com/oheunchan07/TIL/assets/131967057/4e154c3b-6b70-4636-8f50-b7e4c2988bba)

## Bubble Sort 장단점
### 장점
* 구현하기 정말 쉽다.

### 단점
* 하나의 원소가 가장 왼쪽에서 가장 오른쪽으로 이동하기 위해서는 배열에서 모든 다른 원소들과 교환되어야 한다.  
*  가장 왼쪽에서 가장 오른쪽으로 이동하기 위해서는 배열에서 모든 다른 요소들과 교환되어야 한다.  
* 위에 이유로 정렬 중에 시간이 가장 오래 걸린다.

## Bubble Sort 시간 복잡도
> 최상, 최악, 평균이 모두 같다.  
> T(n) = O(n^2)

## Bubble Sort 코드
```
public static void Bubble_Sort(int[] a, int size) {
	for(int i = 1; i < size; i++) {			
		for(int j = 0; j < size - i; j++) {
			if(a[j] > a [j + 1]) {
				int temp = a[i];
		 		a[i] = a[j];
	    	a[j] = temp;
			}
		}      
	}
}
```
