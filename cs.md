## Hash table
- Key-value의 map 자료구조. hash function을 사용하여 index를 bucket의 배열로 계산
- index를 가져오기 위한 hashfunction은 해시출동이 발생가능 두개 이상의 다른 Key에 대해 hash function이 같은 index를 리턴한다. 해결방법은 linkedList에 넣고 노드를 일일이 비교함으로 해결가능, 시간복잡도는 O(1) 최악은 O(N)

## REST란, RESTFUL API 설명
 - REpresentatinal State Transfer
 - 자원을 이름으로 구분하여 자원의 상태를 주고받는 모든것
 - HTTP 프로토콜을 활용하여 웹의 최대 장점을 활용할 수 있는 아키텍처 스타일
 - Clinet-Server 사이의 통신방식
 - HTTP URI를 통해 자원을 명시하고, HTTP Method를 통해 자원에 대한 CRUD 오퍼레이션을 적용하는 것
 - HTTP 프로토콜을 이용하므로 rest api 사용을 위한 별도의 인프라 구축 필요 x
 - HTTP 프로토콜을 사용하는 모든 플랫폼에서 사용가능
 - 의도하는 바를 명확하게 나타나므로 의도를 쉽게 알 수 있음
 - API ? REST 기반으로 서비스 API를 구현
 - 확장성과 재사용을 높여 유지보수 용이

## Thread vs Process
 - 프로세스는 OS에 실행되는 하나의 프로그램
 - 스레드는 프레세스로부터 자원을 할당받아 실행되는 것

## HTTPS
 - 기존 HTTP는 평문으로 데이터 전송이 되기 때문에 제 3자에 의해서 데이터 조작이 될 수 있다. 이러한 것을 보완하기 위해 암호화나 인증구조를 더한 것을 HTTPS(HTTP + SSL) 대칭키 방식과 공개키 방식을 혼합하여 정보를 암호화

## 객체지향 vs 절차지향
 -  절차지향은 순차적으로 처리를 하기 때문에 속도가 빠름, 객채지향 언어는 상속 다형성 등을 사용하여 코드의 재사용성을 높임
 
## 데이터타입과 변수의 차이, 
 - 데이터타입은 프로그래밍언어에서 쓰일 수 있는 데이터의 종료를 말함, 메로리에 저장할 때 확보해야하는 메모리의 공간과 크기를 할당
 - 변수는 데이터를 저장해 놓은 일종의 저장공간, 데이터를 저장할 수 있도록 이름을 할당받은 메모리공간이다

## 왜 char type vs String type 나뉘어졌는지
char는 1개의 문자만 오며, 스트링은 0~ 많은 문자들이 온다. char는 Primitive type, String referenece type

## hashcode 란? hashcode를 이용해서 객체가 같은지 어떻게 비교
 - 객체를 식별할 수 있는 하나의 정수값, Object의 해시코드는 객체의 메모리번지를 이용해서 해시코드를 만들어 리턴, 논리적 동등 비교 시 Hashcode를 오버라이딩(HashSet, HashMap, HashTable) 같은 내용의 key 객체여도 다른 hashcode를 가질 수 있기 때문에 오버라이드 해줘야함

## String pool ?
 - String=""로 생성한다면 힙 영역에 있는 스트링 풀이라는 곳에 생성된다. intern()메서드를 통해 존재한다면 그 값을 반환하고 아니면 거기에 다시생성

## stack 영역에 저장되는 변수가 언제 해제가 되는지
 - 해당 지역변수의 데이터 값이 저장되는 함수가 호출될 때 할당되고 종료되면 해제

## 자바의 대표 컬렉션에는 어떤것 ?
 - List, Map, Set, Stack, Queue


## List, Set, Map의 차이는 무엇인가요?
 - 리스트는 배열과 비슷한 자바의 자료형으로 배열보다 편리한 기능을 가지고 있음.
 - ArrayList는 백터를 개선한 리스트, 배열과 같은 자료구조로 연산수행속도는 배열과 같음
 - LinkedList는 다음 노드의 주소를 기억하고 있는 List로, 삽입 삭제에 용이, 탐색은 처음 노드부터 탐색하여 느림
 - 맵은 키와 밸류 형태
 - HashMap은 key 값에 해시함수를 적용하여 나온 Index value를 저장하는 형식. 중복 허용하지 않고 순서가 없다는 것이 특징
 - TreeMap Red-black tree 자료구조를 이용하고, 어느정도 순서보장
 - LinkedHashMap LinkedList로 구현되어 순서가 보장. 랜덤접근에서는 느림
 - Set 집합을 정의하며 요소의 중복을 허용하지않음.
 - HashSet 접근속도가 빠르고 순서 보장이 안됨 
 - LinkedHashSet 추가된 순서, 가장 최근에 접근한 순서대로 접근가능

## forEach를 사용할 수 있는 자료구조는 어떠한 인터페이스를 상속받고 있나요?
 - Iterator

## Iterator vs Itreable
 - hasNext, next 등을 통해 현재위치, 다음 element

## 배열은 size가 변경될 수 있나요?
 - 배열은 변경될 수는 없지만, 새로 생성해서 복사하는 방법으로 하면 된다

## None Generic 타입의 자료구조는 종류는 무엇이 있나요?
 - 클래스나 메소드 내부에 사용했을 때 컴파일시 미리 지정하는 방법이므로 객체 타입의 안정성을 높일 수 있다.

## 제네릭 타입의 자료구조 장점은? Object로 해도 되는대?
 - 다시 Object로 형변환해야한다.

## ArrayList와 LinkedList의 차이를 설명할 수 있나요?
 - arrayList는 배열로 구현되어있어 물리적순서와 논리적 순서가 일치, LinkedList는 다음 데이터의 정보만 가지고 있어 물리적순서와 논리적 순서가 일치하지 않음

## 데이터를 순차적으로 찾을때 가장 적합한 것은?
 - ArrayList가 적합하다. 데이터를 추가 할때는 추가할 위치 앞까지는 그대로 복사하여 추가한 다음 나머지 데이터 추가. 즉 복사로인해 성능 안좋음

## 데이터를 빈번하게 추가, 삭제할때 가장 적합한것은? 왜 그렇게 생각하시나요?
 - LinkedList가 적합, 데이터를 추가 삭제할 경우 주소값만 바뀌기 때문에 빠름

## ArrayList나 List에서 중간에 데이터를 삭제하면 내부적으로 어떻게 동작하는지 아시나요?
 - ArrayList는 추가,삭제를 위해 임새배열을 생성해 데이터를 복사 사용(대량의 자료를 추가.삭제하면 그만큼 복사가 많이 일어나 성능저하) O(1), O(N)
 - LinkedList는 각 노드가 이전노드와 다음도르의 상태만 알고있음. O(1), O(N)

## LinkedList에서 중간에 데이터를 삽입하면 내부적으로는 어떻게 동작할까요?\

## MAP은 다른 자료구조와 무엇이 다른가요?
 - List, Set은 순서나 집합적인 개념이라면 Map은 검색적인 개념이다.

## 알고있는 MAP의 종류는?
 - HashMap: Key value 형태로 둘 다 null을 허용하고, key는 중복을 허용하지 않으며, 키와 값이 저장되는 위치를 경정하므로, 사용자는 위치를 알 수없다.
 - LinkedHashMap: HashMap을 상속받으며 입력한 순서대로 데이터를 저장.
 - TreeMap: Map 인터페이스와 SortedMap 인터페이스를 구현한 클래스로 정렬 기능이 지원되는 Map. 정렬을 지원하고 데이터를 얻어오는 속도가 빠름

## HashTable과 HashMap의 차이는 무엇인가요?
 - HashMap은 비동기화 되어있어 스레드 세이프하지 않음, HashTable은 스레드 세이프하다. 여러개의 스레드를 작업할 때 HashTable을 써야함
 - HashTable은 key value에 널 허용하지않는다.
 - HashMap은 반복적으로 객체들을 가져오기 위해 Iterator 사용, HashTable은 vector와 달리 enum을 사용하는 유일한 클래스
 - 속도는 HashMap이 비동기화이기때문에 빠르고 메모리를 적게사용.

## Hashing이란 무엇인가요?
 - 해싱은 하나의 문자열을 원래의것을 상징하는 더 짧은 길이의 값이나 키로 변환

## Hash값은 중복될 수 있는데 Hash의 충돌을 피할 수 있는 방법은 무엇인가요?
 - 체이닝 : 연결리스트로 데이터를 연결하는 방식
 - 개방주소법 : 해시충돌이 일어나면 다른 버켓에 데이터를 삽입하는 바익

## Hashing을 하면 어떤 점이 좋고 왜 해야되나요?

## Queue와 Stack을 사용하는 예를 들어주세요.
 - Stack: 첫번째르 들어온 데이터가 제일 마지막에 나가는 자료구조
 - Queue: 첫번째로 들어온 데이터가 제일 처음으로 나가는 자료구조

## Queue와 Stack은 내부적으로 어떤 자료구조를 사용하는지 알고 있나요?
 - Stack은 ArrayList가 적당하고, Queue는 LinkedList 

## Vector
 - 벡터는 get set 역할을 하는 모든 메서드에 synchronized가 붙어있음
 - 모든 메서드에 synchronized가 붙어있으면 쓸데없는 locking이 걸려 오버헤드가 발생한다.
 - Java의 Vector와 Stack은 멀티스레드 환경의 여부와 상관없이 대부분의 조건에서 성능 저하를 일으킨다.Vector가 필요한 상황이라면 대신 ArrayList를 사용하는 것이 바람직하다. 마찬가지로 Stack 대신 Deque의 하위컬렉션을 상황에 맞게, 혹은 그냥 ArrayList를 사용하는 것이 적절하다.

## 스택 두개로 큐 구현
```java

public class Practice {
    static class Queue<T> {
        Stack<T> stackNew;
        Stack<T> stackOld;

        Queue(){
            stackNew = new Stack<>();
            stackOld = new Stack<>();
        }

        public int size() {
            return stackOld.size() + stackNew.size();
        }

        public void add(T value){
            stackNew.push(value);
        }

        public void shiftStack() {
            if(stackOld.isEmpty()) {
                //while(!stackNew.isEmpty()) {
                    stackOld.push(stackNew.pop());
                //}
            }
        }

        public T peek() {
            shiftStack();
            return stackOld.peek();
        }

        public T remove(){
            shiftStack();
            return stackOld.pop();
        }
    }
    public static void main(String[] args) {
        Queue<Integer> q= new Queue<Integer>();
        q.add(1);
        q.add(2);
        q.add(3);

        System.out.println(q.remove());
        System.out.println(q.remove());
        System.out.println(q.remove());

        q.add(4);
        q.add(5);
        q.add(6);

        System.out.println(q.remove());
        System.out.println(q.remove());
        System.out.println(q.remove());
    }
}

```

## 트리 선회방법
```
     1
    / \
   2   3
  / \
 4   5
```
 - 중위(InOrder)  : Left->Root->Right 4 2 5 1 3
 - 전위(PreOrder) : Root->Left->Right 1 2 4 5 3
 - 후위(PostOrder): Left->Right->Root 4 5 2 3 1

## Tree는 어떤 경우에 사용을 하나요? 다른 자료구조랑 어떤 차이가 있나요?
 - 

B-Tree에 대해 설명할 수 있나요? 노드가 어떻게 되어있나요?

## 이진검색트리(Binary Search Tree)에 대해 설명할 수 있나요?
 - 최대 2개인 노드들로 구성된 트리, 탐색알고리즘에 많이 구현됨
 - O(log n)
 - 값에 따라 곧바로 위치가지정되어 검색이빠름
 - 단점: 최악의 경우 한쪽으로만 이어질 수 있다.

## DFS vs BFS
 - DFS : 노드부터 시작해서 다음 분기로 넘어가기전에 해당분기를 완벽하게 탐색(방문했던 체크해야함, 재귀)
 - BFS : 루트 노드로 부터 시작해 가장 인접한 노드를 탐색(재귀로 동작 x, queue,방문했던 체크해야함 )

이진검색트리에서 검색속도가 가장 느린케이스는 데이터가 어떻게 저장되어 있는 경우인가요?

## 동기화를 지원하는 자료구조는 어떤것들이 있나요?
 - List : vector
 - Map : ConcurrentHashMap (동기화 시 hashtable을 전체에 대해 lock을 걸지않고 조각을 쪼개어 부분 부분을 lock을 걸어 성능을 높임)
 - HashTable

## 동기화를 지원하는 자료구조는 왜, 언제 필요할까요?
 - 하나의 스레드를 안전하게 처리하도록 도와줌, 멀티스레드환경에서 하지만 서능이 느려진다 lock이 걸리기때문에, 스레드가 병렬적으로 작업할 수 있도록 java.util.concurrent 패키지에 ConcurrentHashMap, ConcurrentLinedQueue 제공

멀티쓰레드 환경에서 동기화를 지원하지 않으면 어떤문제가 발생하나요?





