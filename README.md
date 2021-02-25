# Algorithm_DIvide_and_Conquer_Backtracking

### Divide and Conquer
- 설계 전략
  - 분할(Divide) : 해결할 문제를 여러 개의 작은 부분으로 나눔
  - 정복(Conquer) : 나눈 작은 문제들을 각각 해결
  - 통합(Combine) : 해결된 해답을 모음
  
#### 병합 정렬(Merge Sort)
- 여러 개의 정렬된 자료의 집합을 병합하여 한 개의 정렬된 집합으로 만드는 방식
- Divide and Conquer 사용
  - 자료를 최소 단위의 문제까지 나눈 후에 차례대로 정렬하여 최종 결과를 얻음
  - top-down
- 시간 복잡도 : O(n log n)
- [코드](https://github.com/KimUJin3359/Algorithm_DIvide_and_Conquer_Backtracking/blob/master/MergeSort/MergeSort/main.cpp)
  - 분할
    - 더 이상 나눠지지 않을 떄(크기가 1)까지 분할
  - 정복 & 병합
    - 합치는 각 배열의 첫번째 원소를 비교하여 더 작은 값을 선택하여 배열에 삽입
- 외부 정렬의 기본이 되는 정렬 알고리즘
- 멀티코어 CPU나 다수의 프로세서에서 정렬 알고리즘을 병렬화하기 위해 병합 정렬 알고리즘 사용    

#### 퀵 정렬(Quick Sort)
- 주어진 배열을 두개로 분할하고, 각각을 정렬하는 점은 병합 정렬과 동일
- 다른점
  - 기준이 되는 기준점(pivot)을 중심으로, 작은 값들과 큰 값들로 나눔
  - 나뉜 값들을 재정렬해 나가기 때문에 통합 작업이 필요하지 않음
- 시간 복잡도 : 평균적으로 n log n의 시간 복잡도를 보이나, 최악의 경우 n^2
  - 그럼에도 병합 정렬을 사용하지 않고 퀵 정렬을 사용하는 이유는 공간적 효율성 때문(병합 정렬은 별도의 배열 필요)
- [코드](https://github.com/KimUJin3359/Algorithm_DIvide_and_Conquer_Backtracking/blob/master/QuickSort/QuickSort/main.cpp)  
  - 분할
    - pivot을 기준으로 더 작은 값은 왼쪽, 더 큰 값은 오른쪽으로 분리
    - 각 각의 나눠진 부분에서 다시 기준점을 잡아 정렬
- 매우 큰 입력 데이터에 대해서 좋은 성능을 보이는 알고리즘

#### 이진 검색(Binary Search)
- 자료의 가운데에 있는 항목의 키 값과 비교하여 다음 검색의 위치를 결정하고 검색을 계속 진행
  - 목적 키를 찾을 떄까지 이진 검색을 순환적으로 반복 수행함
  - 검색 범위를 반으로 줄여가면서 보다 빠르게 검색을 수행
- 자료가 정렬된 상태여야 함  

### Back Tracking

    
    
    
