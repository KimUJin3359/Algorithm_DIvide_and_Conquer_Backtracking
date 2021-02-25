## Algorithm_DIvide_and_Conquer_Backtracking

### Divide and Conquer
- 설계 전략
  - 분할(Divide) : 해결할 문제를 여러 개의 **작은 부분**으로 나눔
  - 정복(Conquer) : 나눈 작은 문제들을 각각 해결
  - 통합(Combine) : 해결된 **해답을 모음**
  
#### 병합 정렬(Merge Sort)
- 여러 개의 정렬된 자료의 집합을 병합하여 한 개의 정렬된 집합으로 만드는 방식
- Divide and Conquer 사용
  - 자료를 최소 단위의 문제까지 나눈 후에 차례대로 정렬하여 최종 결과를 얻음
  - top-down
- 시간 복잡도 : O(n log n)
- [코드](https://github.com/KimUJin3359/Algorithm_DIvide_and_Conquer_Backtracking/blob/master/MergeSort/MergeSort/main.cpp)
  - 분할
    - **더 이상 나눠지지 않을 떄(크기가 1)까지** 분할
  - 정복 & 병합
    - 합치는 각 배열의 첫번째 원소를 비교하여 더 작은 값을 선택하여 배열에 삽입
- 외부 정렬의 기본이 되는 정렬 알고리즘
- 멀티코어 CPU나 다수의 프로세서에서 정렬 알고리즘을 병렬화하기 위해 병합 정렬 알고리즘 사용    

#### 퀵 정렬(Quick Sort)
- 주어진 배열을 두개로 분할하고, 각각을 정렬하는 점은 병합 정렬과 동일
- 다른점
  - 기준이 되는 **기준점(pivot)을 중심**으로, 작은 값들과 큰 값들로 나눔
  - 나뉜 값들을 재정렬해 나가기 때문에 통합 작업이 필요하지 않음
- 시간 복잡도 : 평균적으로 n log n의 시간 복잡도를 보이나, 최악의 경우 n^2
  - 그럼에도 병합 정렬을 사용하지 않고 퀵 정렬을 사용하는 이유는 공간적 효율성 때문(병합 정렬은 별도의 배열 필요)
- [코드](https://github.com/KimUJin3359/Algorithm_DIvide_and_Conquer_Backtracking/blob/master/QuickSort/QuickSort/main.cpp)  
  - 분할
    - pivot을 기준으로 더 작은 값은 왼쪽, 더 큰 값은 오른쪽으로 분리
    - 각 각의 나눠진 부분에서 다시 기준점을 잡아 정렬
- **매우 큰 입력 데이터**에 대해서 좋은 성능을 보이는 알고리즘

#### 이진 검색(Binary Search)
- 자료의 **가운데에 있는 항목의 키 값과 비교**하여 다음 검색의 위치를 결정하고 검색을 계속 진행
  - 목적 키를 찾을 떄까지 이진 검색을 순환적으로 반복 수행함
  - 검색 범위를 반으로 줄여가면서 보다 빠르게 검색을 수행
- 자료가 정렬된 상태여야 함  

### Back Tracking
- 여러 가지 선택지들이 존재하는 상황에서 한가지를 선택
- 선택이 이루어지면 새로운 선택지들의 집합이 생성
- 선택을 반복하며 최종 상태에 도달
  - 올바른 선택을 계속하면 목표 상태에 도달

#### 깊이 우선 탐색과의 차이
- **가지치기** : 어떤 노드에서 출발하는 경로가 해결책으로 이어질 것 같지 않으면 **더이상 그 경로를 따라가지 않음**
- 일반적으로 깊이 우선 탐색에 비해 경우의 수가 줄어들지만 이 역시 최악의 경우에는 지수함수 시간을 요함

### Tree
- 트리는 싸이클이 없는 무향 연결 그래프
  - 두 노드 사이에는 유일한 경로가 존재
  - 각 노드는 최대 하나의 부모 노드가 존재 가능
  - 각 노드는 자식 노드가 없거나 하나 이상 존재
- 비선형 구조
  - 원소들 간에 1 : n 관계를 가지는 자료구조
  - 원소들 간에 계층 관계를 가지는 계층형 자료구조
- [이전 정리 내용](https://github.com/KimUJin3359/Algorithm_List-Tree#%ED%8A%B8%EB%A6%AC)

### Index Tree
- **추가 예정**

#### 관련 문제    
- [1.Best Way(SW Expert Academy : 최적경로)](https://github.com/KimUJin3359/Algorithm_DIvide_and_Conquer_Backtracking/blob/master/BestWay/BestWay/main.cpp)
  - [문제](https://swexpertacademy.com/main/talk/solvingClub/problemView.do?solveclubId=AXc2524K9JYDFAWs&contestProbId=AV15OZ4qAPICFAYD&probBoxId=AXfMntvaYoMDFAUO&type=PROBLEM&problemBoxTitle=Day+11%28Divide+and+Conquer+%26+BackTracking%29&problemBoxCnt=2)
  - 회사에서 고객의 위치를 전부 들린 후 집에 도착할 때, 최단 거리를 구하는 문제
  - 접근 방법
    - 백트래킹 : 현재 구하고 있는 거리가 이전의 목표지점에 도착했을 때의 거리보다 길다면 그 경로는 더이상 보지 않음
- [2.Find Common(SW Expert Academy : 공통조상)](https://github.com/KimUJin3359/Algorithm_DIvide_and_Conquer_Backtracking/blob/master/FindCommon/FindCommon/main.cpp)
  - [문제](https://swexpertacademy.com/main/talk/solvingClub/problemView.do?solveclubId=AXc2524K9JYDFAWs&contestProbId=AV15PTkqAPYCFAYD&probBoxId=AXfMntvaYoMDFAUO&type=PROBLEM&problemBoxTitle=Day+11%28Divide+and+Conquer+%26+BackTracking%29&problemBoxCnt=2)
  - 간선과, 정점이 주어짐
  - 두 정점이 주어질 때 가장 가까운 공통 조상을 구하고, 그 조상의 subtree의 크기를 구하는 문제
  - 접근 방법
    - 주어진 간선을 바탕으로 tree를 구성
    - 주어진 정점의 각각 parent node를 찾음
    - 공통된 parent 중 가장 가까운 parent를 찾고, 그 subtree의 크기를 반환

- [3.Tree Recursion(백준 : 트리의 순회)](https://github.com/KimUJin3359/Algorithm_DIvide_and_Conquer_Backtracking/blob/master/TreeRecursion/TreeRecursion/main.cpp)
  - [문제](https://www.acmicpc.net/problem/2263)
  - 트리의 inorder, postorder가 주어졌을 때, preorder을 구하는 문제
  - 접근 방법
    - postorder의 가장 끝 node는 root node
    - inorder에서 위의 root node를 기준으로 다시 왼쪽, 오른쪽 sub tree를 나눌 수 있음
    - sub tree에서 다시 root node를 찾고, 왼쪽 오른쪽 나누기 반복
