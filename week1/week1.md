# Week 1 - 자료구조와 Stack, Queue, Deque


## 자료구조

### 자료구조란?
1. 데이터를 표현하고 저장하는 방법
2. C에서 사용하는 변수, 구조체 등등 모든 것이 자료구조
3. 데이터를 효율적으로 관리하기 위해 학습

### 자료구조의 분류
1. 선형구조
   - 리스트
   - 스택
   - 큐
   - 큐
2. 비선형구조
   - 트리
   - 그래프
3. 파일구조
   - 순차파일
   - 색인파일
   - 직접파일
4. 단순구조
   - 정수
   - 실수
   - 문자
   - 문자열

## Stack
### 개념적 정의
LIFO(Last-In, First-Out) 먼저 저장된 데이터가 나중에 나오는 구조
예시) 프링글스 통(마지막에 들어간 감자칩을 먼저 먹는다)
### 기능적 구성
1. Stack에 데이터를 저장한다 - Push
2. Stack에서 데이터를 꺼낸다 - Pop
3. Stack에 가장 마지막에 저장된 데이터를 확인한다 - Peek
### Operations
```
void Init(Stack *stack);
- 스택의 초기화를 진행한다
- 스택 생성 후 제일 먼저 호출되어야 하는 함수이다

int IsEmpty(Stack *stack);
- 스택이 비어있는 경우 1, 그렇지 않은 경우 0을 반환한다
- Boolean형을 지원할 경우 True, False로 대체 가능하다

void Push(Stack *stack, Data data);
- 스택에 데이터를 저장한다

Data Pop(Stack *stack);
- 마지막에 저장된 데이터를 삭제한다
- 삭제된 데이터는 반환한다
- 단 본 함수의 호출을 위해서는 데이터가 하나 이상 스택에 존재해야 한다

Data Peek(Stack *stack);
- 마지막에 저장된 데이터를 반환하되 삭제하지 않는다
- Pop과 마찬가지로 데이터가 하나 이상 스택에 존재해야 한다
```
### 배열 기반 Stack 구현
1. ArrayStack 구조체를 생성하여 사용한다
2. 구조체 내부에는 데이터 저장을 위한 stackArr배열과 마지막 저장된 위치를 기록하는 topIndex 변수를 정의한다
3. 가장 마지막 저장된 위치를 Stack에서는 top이라고 한다
4. 위 Operation을 구현한다
