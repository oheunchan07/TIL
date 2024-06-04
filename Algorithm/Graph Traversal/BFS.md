# BFS

## BFS란?
> BFS는 `Breadth Fitst Search`의 약자로 너비 우선 탐색이라고 불린다.  
> 현재 가까운 노드를 우선으로 넓게 탐색하는 방법이다.  
> 현재 노드의 이웃 노드를 큐에 집어넣어 자연스럽게 먼저 들어간 노드를 먼저 탐색 하게 되는 방식이다.

## BFS 동작 순서
1. 루트 노드를 큐에 넣고 방문 처리를 한다.
2. 큐를 Deque 하고, Deque 한 노드의 방문하지 않은 모든 인접 노드를 큐에 넣고 방문 처리한다.
3. 위에 단계를 더 이상 수행하지 못할 때 까지 반복한다.

## BFS 구현
```java
static String bfs(int start, int[][] graph, boolean[] visited) {
    StringBuilder sb = new StringBuilder();
    Queue<Integer> q = new LinkedList<Integer>();

    q.offer(start);
		
    visited[start] = true;
		
    while(!q.isEmpty()) {
        int nodeIndex = q.poll();
        sb.append(nodeIndex + " -> ");
        for(int i=0; i<graph[nodeIndex].length; i++) {
            int temp = graph[nodeIndex][i];
            if(!visited[temp]) {
                visited[temp] = true;
                q.offer(temp);
            }
        }
    }
    return sb.toString() ;
}
```