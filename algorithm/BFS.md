# BFS 알고리즘

## 개념

- Queue 자료구조를 사용한다
- 그래프를 표현할 때는 배열을 활용한다
- 모든 노드를 한 번씩 탐색하기 위한 기본적인 방법
- (모든 간선 길이가 동일할 때) 최단 거리를 탐색할 때 사용할 수 있다

## 흐름

1. 시작 노드를 큐에 넣고 [방문 처리]
2. 큐에서 원소를 꺼내 방문하지 않은 인접 노드 유무 확인
   1. 있다면 해당 노드를 큐에 삽입하고 [방문 처리]
3. 큐가 빌 때까지 반복

## 사용 예시

1. 간선 비용이 동일한 상황에서 최단 거리 계산
2. 완전 탐색을 위해 DFS를 사용했는데 메모리/시간 초과를 받아 BFS로 재시도해야할때
3. 보통 코딩테스트에서 DFS로 해결할 수 있는 문제는 BFS로도 해결할 수 있는 경우가 많다

## 문제 풀이 로그

- [백준 18352 특정 거리의 도시 찾기 풀이](https://github.com/heeji289/js-problem-solving/blob/main/graph-traversal/boj18352_%ED%8A%B9%EC%A0%95%EA%B1%B0%EB%A6%AC%EC%9D%98%EB%8F%84%EC%8B%9C%EC%B0%BE%EA%B8%B0_%EC%B5%9C%EB%8B%A8%EA%B1%B0%EB%A6%ACBFS.js)

## TIPS 💡

- Queue를 만들 때, enqueue, dequeue 시 습관적으로 index 0에 접근하고, push로 추가하고 있음. 첫 요소에 접근할 때는 `headIndex로`, 새로 추가할 때는 `tailIndex로` 명심
- 만약 BFS로 방문하면서 graph distance를 기록하고 싶다면, while 문에서 dequeue해온 노드의 distance에 +1을 해주면 된다 (최단거리 기록시)
- Number로 바꾸고 싶다면 `answer.map(Number)`로 단축 가능
