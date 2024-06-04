# DFS

## DFS란?
> DFS는 `Depth First Search`의 약자로 깊이 우선 탐색이라고 불린다.  
> 루트 노드에서 시작해 다른 브랜치로 넘어가기 전에 현재 브랜치의 가장 깊은 노드 까지 탐색하는 방법이다.  
> 가장 깊은 노드에 도달하였을 때 되돌아오기 위해 `스택`이나 `재귀`를 사용한다.  

## DFS 동작 순서
1. 루트 노드를 스택에 넣고 방문 처리를 한다.
2. 스택 최상단 노드의 인근 노드 중 가장 가까운 노드 하나를 스택에 넣는다. 만약에 노드가 존재하지 않는다면 스택을 pop한다.
3. 위에 단계를 더 이상 수행하지 못할 때 까지 반복한다.

## DFS 구현
### 재귀를 통한 구현
``` java
static void dfs(int nodeIndex) {
    vistied[nodeIndex] = true;

    System.out.print(nodeIndex + " ");

    for (int node : graph[nodeIndex]) {
        if(!vistied[node]) {
            dfs(node);
        }
    }
}
```

### 스택을 통한 구현
``` java
public static void main(String[] args) {
		
    stack.push(1);
    vistied[1] = true;
		
    while(!stack.isEmpty()) {
			
        int nodeIndex = stack.pop();
			
        System.out.print(nodeIndex + " ");
			
        for (int LinkedNode : graph[nodeIndex]) {
            if(!vistied[LinkedNode]) {
                stack.push(LinkedNode);
                vistied[LinkedNode] = true;
            }
        }
    }
}
```