---
layout: single
title: "인공지능입문 3주차 수업 정리"
---
## [ 인공지능입문 - 김상연 교수님 강의 ]
2024년 9월 16일, 9월 18일 수업




# 3단원 : 탐색의 개념과 기초

---

### Page 3 : 탐색이란?

1. **탐색이란?**
    - 원하는 것을 찾거나 ***목표 도달에 도움이 되는*** 결과를 추구하는 과정
    - 목표를 향해 가능한 지능적인 활동을 말함.
2. **컴퓨터 과학 분야에서의 탐색**
    - 주어진 데이터 집합에서 원하는 데이터를 찾는 과정을 의미함
        - 검색 엔진에서 원하는 검색어에 따른 검색 결과를 보는 것과 같은 맥락
        - 데이터의 종류에 따른 탐색 기법이 달라지게 된다.
            → 따라서 배열, 트리, 그래프와 같은 탐색 기법이 자료구조에 의존하고 있음.

### Page 4 : 탐색과 자료구조

1. **탐색과 자료구조의 관계**
    - 구조가 비교적 단순한 데이터를 대상으로 하는 탐색 기법
        - 예) 순차, 이진 탐색 등
            → 배열처럼 비교적 단순한 자료구조에서 탐색을 수행함.
              → 예) 학생의 이름과 학점이 적힌 정보들을 찾고자 할 때
          ![image](https://github.com/user-attachments/assets/b3b1370d-558e-4232-a86b-bc5ce64a9427)


### Page 5 : 무작위 탐색(Random Search)

1. **무작위 탐색이란**
    - 어떠한 정보들을 체계적으로 분류하거나 정리할 필요 없이 정말 무작위로 찾는 과정
        - 예) 배열에서 무작위로 index를 뽑아서 해당 내용을 확인하는 방식
2. **무작위 탐색의 장점**
    - 운이 좋을 경우 원하는 정보를 적은 횟수 안에 찾을 수 있음.
3. **무작위 탐색의 단점**
    - 지능적인 탐색은 아니기에 원하는 정보를 찾는데 오히려 시간이 더 소요될 수 있음.
      ![image](https://github.com/user-attachments/assets/e64eee39-6447-428d-9c41-b8fae7aceae3)


### Page 6 : 순차 탐색(Sequential or Linear Search)

1. **순차 탐색이란**
    - Sequential: 순차적으로, 순서가 있는
    - Linear: 선형적으로 나열된 자료들을 탐색하기에
2. **순차 탐색의 예**
    - 정보들을 차례대로 배열 → 탐색
    - 이름 순서대로 정보들을 정렬 → 탐색
        → 어떠한 기준대로 정렬이 된 것이기에 보다 효율적으로 가능하다.
      ![image](https://github.com/user-attachments/assets/22127d1c-ffd0-4d3b-8e0b-a560a06f9e83)


### Page 7 : 이진 탐색(Binary Search)

---

1. **이진탐색이란**
    1. 어떠한 기준으로 정렬된 데이터들의 묶음에서 중간지점부터 탐색한다.
    2. 중간을 탐색하고 찾고자 하는 내용과 중간 것을 비교한다.
    3. 중간을 기준으로 좌우 중 어떤 부분에 목표가 더 가까운지를 판단하면서 탐색 범위를 좁혀 나간다. 

2. **이진탐색의 예**
    1. 이름을 탐색할 때, ㄱ부터 ㅎ까지 정렬된 이름들에서 ㅈ으로 시작하는 사람을 찾고자 할 때 → 가운데 쯤인 ㅅ부터 탐색 → 이후 ㅈ은 ㅅ보다 뒤니 ㅅ 이전 절반은 탐색하지 않음.
    2. 1부터 100까지의 숫자 중에서 75를 찾을 때 → 50부터 검색 → 75는 50보다 크니 50 이하는 탐색 제외 → 다음 중간이 75 탐색 → 목표 달성

3. **이진탐색의 장점**
    1. 탐색 횟수를 많이 줄일 수 있음.
    2. 다른 순차 탐색이나 무작위 탐색보다 훨씬 효율적임.
![image](https://github.com/user-attachments/assets/1298aa97-073d-4864-b660-e7f9d98e5a81)

---

### Page 8 : 탐색을 통한 문제 풀이 (Problem-solving)

---

1. **인공지능 에이전트에서의 탐색 알고리즘의 활용**
    1. 일반적으로 문제 풀이 상황에서 탐색 알고리즘을 활용한다.
        1. 문제 풀이 상황: 미로찾기, 길찾기, 틱택토, 체스, 바둑 등 복잡한 상태를 해결하는 상황
        ![image](https://github.com/user-attachments/assets/e03a919b-907f-48c1-958d-ec7693969e1d)


2. **문제 해결 에이전트 (Problem-solving Agent)**
    1. 문제 풀이 상황처럼 쉽게 목표를 달성할 수 없는 상황에서
    → 적절한 미래 계획을 수립할 수 있는 인공지능 에이전트

3. **탐색**
    1. 에이전트가 목표 상태로의 경로를 형성하는 동작열(동작들의 집합)을 산출하는 계산 과정을 말함.

---

### Page 9 : 인공지능 탐색의 활용 분야

---

- 탐색은 인공지능 기법으로 최근 각광받고 있는 알파고에도 활용됨.
- 탐색 기법은 지도 및 네비게이션, 온라인 게임 등의 분야에도 사용되며, 인공지능 기술의 기반 기술로 활용됨.
- **활용 예시 분야**: 최적화 분야, seq2seq 모델 beam search 등

---

### Page 10 : 탐색 문제와 해

---

1. **상태공간 (State Space)**: 환경의 가능한 상태로 이루어진 전체 집합
2. **전이모형 (Transition Model)**: 각각의 동작들이 하는 일을 서술하는 모형, 현재 상태에서 다음 상태로 전이할 때 정의되는 규칙이나 함수
3. **초기상태 (Initial State)**: 에이전트의 최초 상태
4. **목표상태 (Goal State)**: 환경 내에서 추구하는 목표 상태
    - 목표는 단일이거나 여러 개의 목표 집합이 될 수 있음.
5. **연산자 (Operator)**: 에이전트가 하는 액션, 동작
    - 에이전트가 어떤 행동을 했을 때 매번 다음 상태가 변화하므로 연산자라고 불림.
      ![image](https://github.com/user-attachments/assets/6a21e24c-9db1-47f9-bb40-63f3eeaaacd7)


---

### Page 11 : 탐색을 통한 문제 풀이 과정

---

1. **목표 형식화 (Goal Formulation)**: 목표가 분명해지면, 목적이 제한되고 에이전트가 고려할 동작 자체가 줄어들게 된다.
2. **문제 형식화 (Problem Formulation)**: 목표 도달에 필요한 상태와 동작열을 고안하는 것. 목표 달성과 관련된 추상화된 모형 구축
3. **탐색 (Search)**: 목표 도달에 필요한 동작열을 발견할 때까지 앞서 구축한 모형 안에서 모의 실행해서 해(solution)를 찾는다.
    - 해를 찾을 수 없는 경우, 문제 자체를 풀 수 없다는 결론에 도달함.
4. **실행 (Execution)**: 해답에 필요한 동작들을 실행함.


### Page 12 ~ 16 : 표준화된 장난감 문제

---

1. **진공청소기 예제**
    1. **상태(States)**: 에이전트의 위치, 먼지의 위치
        - 에이전트: 왼쪽/오른쪽 중 하나에 있음 - L/R
        - 먼지의 위치: 왼쪽/오른쪽 각각에 있을 수도, 없을 수도 있음.
        - ***가능한 상태 세계: 2(에이전트 위치) * 2(먼지 유무) * 2(먼지 위치) = 8가지*** 
    2. **초기상태(Initial State)**: 8가지 상태 중 어떤 상태든 초기 상태로 지정할 수 있음.
    3. **동작(Actions)**: 왼쪽(Left), 오른쪽(Right), 흡입(Suck)
    4. **전이 모형(Transition Model)**: 3가지 에이전트의 동작들은 예상되는 효과를 가짐
        - 단, 왼쪽 끝에서 다시 왼쪽으로 이동하거나, 오른쪽 끝에서 또 다시 오른쪽으로 이동하거나, 이미 깨끗한 칸을 흡입하는 경우 → 아무런 효과가 없음 → 이에 대한 전이 모형이 필요함.
    5. **목표 상태(Goal State)**: 모든 칸이 깨끗한지 확인하기
   ![image](https://github.com/user-attachments/assets/83a5bc38-c6c0-4ab3-9297-10f6174a9b9a)


---

2. **8-Puzzle**
    - **8-Puzzle이란**: 9개의 칸 중에서 8개의 칸에는 숫자가 있고, 나머지 빈 1개의 칸으로 퍼즐을 움직여서 1부터 8까지의 순서로 정렬하는 것.
    1. **상태(States)**: 8개의 타일과 빈 칸의 위치
    2. **초기상태(Initial State)**: 어떤 상태든 초기 상태로 지정 가능함.
    3. **동작(Actions)**: 왼쪽(Left), 오른쪽(Right), 위(Up), 아래(Down)
        - 8-Puzzle에서의 동작은 ***빈칸을 어디로 보내느냐*** 의 의미를 가짐.
    4. **전이 모형(Transition Model)**: 초기 상태에서 동작이 적용되면 결과 상태에서 타일 위치가 바뀜.
    5. **목표 상태(Goal State)**: 현재 상태가 목표 구성과 일치하는지 확인.
   ![image](https://github.com/user-attachments/assets/47f5fd11-56cf-45df-807f-6a08060e0a46)
        → 9칸을 좌표로 표현하면 (0,0)부터 (2,2)까지 생기게 된다.
        → 좌표를 토대로 리스트를 만들어서 정렬할 수도 있음.
       ![image](https://github.com/user-attachments/assets/e4791aef-d625-4dc7-bcb1-276ce87bb74f)



---

3. **미로 찾기**
    1. **상태(States)**: 미로 내의 에이전트(탐색자)의 위치, 미로의 구조
        - 미로 전체를 x, y로 표현하면 목표 지점과 에이전트의 위치를 좌표로 지정할 수 있음.
        - ***총 x * y 개의 상태가 존재함.***
    2. **초기 상태(Initial State)**: 에이전트가 미로의 시작 지점에 있는 상태.
    3. **동작(Actions)**: 에이전트의 상하좌우(North, South, East, West) 움직임
        - 벽이 있을 경우 해당 방향으로 이동할 수 없음.
    4. **전이 모형(Transition Model)**: 동작이 기대되는 효과를 가짐.
        - ex) 에이전트가 현 위치에서 왼쪽으로 이동 → 해당 위치로 이동, 벽이 있으면 해당 동작은 무효.
    5. **목표 상태(Goal State)**: 미로 내 특정 위치(목표 지점)에 도달하는 것.
       ![image](https://github.com/user-attachments/assets/c979c0ad-c756-44f6-b082-506a96784456)
       ![image](https://github.com/user-attachments/assets/846a0c06-0315-4d87-bccb-6797c2eb4ee6)
       → 모든 분기들을 나열하면 다음과 같다.
       → 이 중에서 가장 깊이가 짧은 것을 선택하면 가장 효율적인 탐색이 된다.



---

### Page 17 : 탐색 상태 표현을 위한 그래프와 트리 구조

---

- **그래프와 트리 구조의 활용**: 다양한 복잡한 문제의 상태공간을 보다 쉽게 표현하고 이해하기 위해 그래프나 트리 구조를 자주 활용함.
- **트리(Tree)**:
    - 그래프의 일종으로 비순환적(acrylic)이고, 방향성(directed)이 있음.
- **그래프(Graph)**:
      ![image](https://github.com/user-attachments/assets/fbd4eeb7-45e1-43cd-9333-fc9ac0f9fa4a)
      → 왼쪽은 그래프, 오른쪽이 트리 구조이다. 

    
---

### Page 18 : 문제 해결 성능 측정

---

**탐색 알고리즘의 성과 평가 척도**

1. **완결성(Completeness)**: 문제에 해답이 있을 때, 그 해답을 찾을 수 있는지 여부.
2. **최적성(Optimality)**: 가장 비용이 낮은 해답, 즉 가장 효율적이고 최적의 답을 찾을 수 있는지 여부.
3. **시간복잡도(Time Complexity)**: 해답을 찾는 데 걸리는 시간.
4. **공간복잡도(Space Complexity)**: 탐색 수행에 필요한 메모리 양.
    - b: 탐색 트리의 최대 분기 계수(너비).
    - d: 목표 노드의 깊이.
    - m: 트리의 최대 깊이.

---

### Page 19 : 복잡도

---

**빅 오 표기법(Big O Notation)**

- **빅 오 표기법**: 입력 크기(n)가 커질 때 필요한 연산 횟수를 모델링한 것.
- **빅 오 표기법을 통해 알 수 있는 것들**:
    - 함수나 알고리즘의 복잡도를 설명할 수 있음.
    - 입력 크기가 증가해도 연산 횟수가 제한적이거나 일정한 알고리즘이 좋은 알고리즘임.
    
- **예시**:
    - Hello World 출력 → O(1)
    - 목록에 있는 항목 출력 → O(n)
    - 한 목록의 항목을 다른 목록과 비교 → O(n^2)

---

**지능형 알고리즘의 주요 목적**: 계산 비용을 최소화하는 것.

→ 문제를 빠르고 효율적으로 해결하기 위해.

![image](https://github.com/user-attachments/assets/9f1ed3bc-9d39-4c43-be95-db4827d5441f)



### 3주차 실습 - 그래프와 트리

---

1. 그래프
    1. 그래프 구조는 노드(혹은 버텍스)와 엣지로 구성된 관계를 나타내는 자료구조임. 
    2. 보통 그래프는 G = (V, E) 로 표현하며, V는 노드의 집합, E는 엣지의 집합을 의미함

2. 인접 행렬과 인접 리스트
    1. 그래프는 인접 행렬 혹은 인접리스트로 표현할 수 있음
       ![image](https://github.com/user-attachments/assets/07557117-7a6b-4ddb-b4aa-619ebd82ada9)

    → 순서대로 그래프, 인접 행렬, 인접리스트
        
        ![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/9e0fcb96-cbd0-499f-add8-257d38028f67/494b7dc3-71cb-4920-88ce-3bc4b57e9dfd/image.png)
        
    2. 인접행렬 구현
        
        ```python
        # 인접 행렬
        
        # node를 정의함. 
        nodes = ['A', 'B', 'C', 'D', 'E']
        
        # 2차원 리스트를 만들어서 인접 행렬을 표현함. 
        # 노드들이 연결되어있으면 1로 표현
        # 노드들이 연결되어있짐 않으면 2로 표현
        adj_matrix = [
          # A B C D E
          [ 0,1,1,0,0 ], # A
          [ 1,0,0,0,0 ], # B
          [ 1,0,0,1,0 ], # C
          [ 0,0,1,0,1 ], # D
          [ 0,0,0,1,0 ]  # E
        ]
        
        # for문을 돌면서 모든 노드들마다 연결된 노드들을 출력함. 
        # 1이라면 연결된 것으로 판단, connected_nodes에 추가하여 출력함. 
        for i in range(len(adj_matrix)):
          connected_nodes = [nodes[j] for j in range(len(adj_matrix[i])) if adj_matrix[i][j] == 1]
          print(f"{nodes[i]} 는 {', '.join(connected_nodes)}와 연결")
        ```
        
        ```python
        # 출력 결과
        
        A 는 B, C와 연결
        B 는 A와 연결
        C 는 A, D와 연결
        D 는 C, E와 연결
        E 는 D와 연결
        ```
        
    3. 인접 리스트 구현
        
        ```python
        # 인접 리스트
        
        # 그래프를 딕셔너리 형태로 표현함. 
        # 각 노드를 key값으로 두고, 연결된 노드들을 value값으로 준다. 
        graph = {
          'A': ['B', 'C'],
          'B': ['A'],
          'C': ['A', 'D'],
          'D': ['C', 'E'],
          'E': ['D']
        }
        
        # for문을 사용해서 graph에서 연결된 노드들을 모두 출력함. 
        for node in graph:
          print(f"{node} 는 {', '.join(graph[node])}와 연결")
        ```
        
        ```python
        # 출력 결과
        
        A 는 B, C와 연결
        B 는 A와 연결
        C 는 A, D와 연결
        D 는 C, E와 연결
        E 는 D와 연결
        ```
        
    b. 그래프는 다양한 유형으로 존재할 수 있음. 
    
    1. 무향성 : 방향이 없는 그래프
    2. 유향성 : 방향이 있는 그래프
    3. 연결이 끊긴 : 일부의 연결이 완전하지 않고 끊긴 그래프
    4. 비순환 : 순환하지 않는 그래프
    5. 완전한 : 모든 노드들이 완전히 연결되어 있는 그래프
    6. 완전 이분 : 2개로 나눠진 영역의 노드들끼리만 이분적으로 연결된 그래프  
    7. 가중치 : 노드들 사이의 가중치가 있어서 엣지에 가중치가 추가된 그래프

3. 트리
    1. 트리 구조 : 노드들이 나뭇가지처럼 연결된 구조
    2. 특징
        1. 비선형적
        2. 계층적 → 방향을 가지고 있음. 
        3. 그래프의 한 형태, 비순환적인 연결 그래프의 일종임 
    3. 트리 구조 용어 
        - 루트 노드(Root) : 시작노드, 맨 위의 최초의 노드
        - 자식 노드(Child Node) : 가지로부터 나온 노드
        - 부모 노드(Parent Node) : 자식 노드를 가지는 노드
        - 리프 노드(Leaf Node) : 맨 마지막에 위치한 노드
        - 형제관계(Sibling) : 같은 레벨에 있고, 같은 부모로부터 나온 노드
        - 이웃관계(Neighbor) : 같은 레벨에 있지만 다른 부모로부터 나온 노드
        - 깊이(level) : 루트노드가 0, 아래로 갈 수록 증가한다.
        
        ![image](https://github.com/user-attachments/assets/725959d6-80fc-41bf-bbd0-7b2ab8df7ac7)

        
    ```python
    # 트리 구조:
    #       1
    #      / \
    #     2   3
    #    / \
    #   4   5
    
    # Tree 생성을 위한 Node
    
    # tree는 class를 사용해서 구현하곤 한다. 
    # data : 각 노드에 있는 값들을 의미함. 
    # 왼쪽 가지와 오른쪽 가지를 정의함. 
    
    class Node:
      def __init__(self, data):
        self.data = data
        self.left = None
        self.right = None
    
    # root를 시작으로 1이라는 값을 넣고 각각 왼쪽, 오른쪽 노드로 이동해가면서 값들을 넣어준다. 
    root = Node(1)
    root.left = Node(2)
    root.right = Node(3)
    root.left.left = Node(4)
    root.left.right = Node(5)
    
    # root의 값, root의 왼쪽 자식노드의 값, root의 왼쪽 자식노드의 왼쪽자식노드의 값을 출력함. 
    print(root.data, root.left.data, root.left.left.data)
    ```
    
    ```python
    # 출력 결과
    
    1 2 4
    ```

4. 8 Puzzle 만들기
- 트리 구조를 활용해 경로 탐색 용이하도록 문제 상황의 상태 공간을 class 로 구현함.
- 상태 정보를 담기 위한 속성
    - board
- 다음 상태로의 전이를 가능하게 하는 전이모형에 해당하는 함수
    - get_new_board : 동작
    - expand : 동작을 통해 확장 가능한 상태를 생성
- 그 외 함수
    - 객체(현재 상태)를 출력해 현재 상태를 확인하는 함수
    - 구 객체(현재 상태 vs 목표 상태)를 비교하기 위한 함수

```python
#클래스 설계 (상태, 전이모형, 그외 함수 포함)

# 트리를 만들기 위한 Puzzle class 생성
class Puzzle:
    
    # 상태 정보를 담기 위한 board를 생성함. 
    def __init__(self, board):
        self.board = board

    # 전이모형 - 동작 : 2개의 노드(=퍼즐)의 위치를 바꾸고 적용된 board를 return하는 함수 
    def get_new_board(self, i1, i2):
        new_board = self.board[:]
        new_board[i1], new_board[i2] = new_board[i2], new_board[i1]
        return Puzzle(new_board)

    # 보드의 인덱스
    # 0, 1, 2
    # 3, 4, 5
    # 6, 7, 8

    # 전이모형 - 확장 가능 상태 생성 : 빈칸의 위치를 통해 가능 상태를 하나의 리스트에 넣어 return하는 함수  
    def expand(self):
        result = []
        i = self.board.index(0)

        # 맨 왼쪽 퍼즐
        if i not in [0,3,6]: # left
            result.append(self.get_new_board(i, i-1))  #왼쪽 이동 = 인덱스 -1

        # 맨 위쪽 퍼즐
        if i not in [0,1,2]: # up
            result.append(self.get_new_board(i, i-3))  #위쪽 이동 = 인덱스 -3

        # 맨 위쪽 퍼즐
        if i not in [6,7,8]: # down
            result.append(self.get_new_board(i, i+3))  #아래쪽 이동 = 인덱스 +3

        # 맨 위쪽 퍼즐
        if i not in [2,5,8]: # right
            result.append(self.get_new_board(i, i+1))  #오른쪽 이동 = 인덱스 +1
        return result
    
    # board를 출력하는 함수 
    def __str__(self):
        return str(self.board[:3]) + "\n" + str(self.board[3:6]) + "\n" + str(self.board[6:9])
    
    # 같은지 비교하는 함수 
    def __eq__(self, other):
        return self.board == other.board
    
    # 다른지 비교하는 함수 
    def __ne__(self, other):
        return self.board != other.board
```python

# 초기 상태 정의

initial_state = [0, 1, 3,
                 4, 2, 5,
                 6, 8, 7]
```

```python
# 초기의 퍼즐 객체 생성

initial_puzzle = Puzzle(initial_state)
```
```python
# 다음상태의 퍼즐의 리스트를 확장하기
next_puzzle_list = initial_puzzle.expand()

# 보기 편하게 출력하기 
for i, v in enumerate(next_puzzle_list):
  print(f"#{i}\n{v}")
```
```python
# 출력 결과

#0
[4, 1, 3]
[0, 2, 5]
[6, 8, 7]
#1
[1, 0, 3]
[4, 2, 5]
[6, 8, 7]
```
