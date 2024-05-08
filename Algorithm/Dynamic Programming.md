# Dynamic Programming

## Dynamic Programming?
> 하나의 큰 문제를 여러개의 작은 문제로 나누어 그 결과를   
> 저장하여 다시 큰 문제를 해결할때 사용하는 것으로 DP라고 불리기도 한다.

## DP사용 조건
> DP를 사용하기 위해선 아래 2조건을 만족해야 한다.
### OverlappingSubproblems(겹치는 부분 문제)
> DP는 기본적으로 문제를 나누고 그 문제의 결과 값을 다시 사용해 전체 답을 구하는 것이다.  
> 그렇기 때문에 해당 부분에 문제가 반복적으로 나타나지 않는다면 재사용이 불가능해서 부분 문제가 중복되지 않는 경우에는 사용할 수 없다.

### Optimal Substructure(최적 부분 구조)
> 부분 문제의 최적 결과 값을 사용해 전체 문제의 최적 결과를 낼 수 있는 결과를 의미한다.  

![image](https://github.com/oheunchan07/TIL/assets/131967057/25734422-1d2c-49ba-972c-5af7529d61ae)
> 만약, A - B까지의 가장 짧은 경로를 찾고자 하는 경우를 예시로 할 때, 중간에 X가 있을 때, A - X / X - B가 많은 경로 중 가장 짧은 경로라면 전체 최적 경로도 A - X - B가 정답이 된다.

## DP구현 방법
### Bottom-Up 
> 이름처럼 아래에서부터 계산을 수행하고 누적시켜 전체 큰 문제를 해결하는 방식이다.  
> dp[0]부터 시작하여 반복문을 통해 점화식으로 결과를 내서 dp[n]까지 그 값을 전이시켜 재활용하는 방식이다.

### Top-Down
> 큰 문제를 작은 문제들로 나누어 해결하는 방식이다.  
> 재귀 함수를 사용하여 문제를 작은 부분 문제들로 쪼개고, 중복 계산을 피하기 위해 이전에 계산한 값을 저장하는 Memoization을 활용한다.

## DP 대표 문제들
[피보나치 수 2](https://www.acmicpc.net/problem/2748)  
[2×n 타일링](https://www.acmicpc.net/problem/11726)  
[1, 2, 3 더하기](https://www.acmicpc.net/problem/9095)  
[퇴사 2](https://www.acmicpc.net/problem/15486)  
[계단 수](https://www.acmicpc.net/problem/1562)  
[경찰차](https://www.acmicpc.net/problem/2618)  