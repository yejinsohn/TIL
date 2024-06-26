## 💭 해시(HASH)란?
해시(Hash)는 key-value쌍으로 이루어진 데이터 구조로 저장 또는 검색 등에서 자주 활용되는 자료구조이다. <br>
해시 구조에서는 key를 이용하여 value를 빠르게 찾을 수 있고, 알고리즘을 어떻게 구현하는지에 따라 용도와 성능이 달라진다!

### 💬 관련 용어
1. **해시 함수(Hash Function)** : 임의의 데이터를 고정된 길이의 값으로 리턴해주는 함수
   > 좋은 해시 함수의 조건 : 빠른 계산 속도와 다양한 결과값 리턴
2. **해시 테이블(Hash Table)** : key와 value를 함께 저장해 둔 데이터 구조로 키 값의 연산에 의해 직접 접근이 가능한 데이터 구조
3. **해싱(Hashing)** : 해시 함수에서 해시를 출력하고, 해시 테이블에 저장하는 과정까지의 행위

<br>

## 💥 해시 충돌 (Hash Collision)
서로 다른 대상이 동일한 해시 값을 가지는 현상


### 🛠️ 해결 방법
1. **분리 연결법(Separate Chaining)** : 충돌이 발생하면 연결된 새로운 공간을 사용하는 방법
   <br>
   <div>
     <img src="https://github.com/yejinsohn/TIL/assets/104317217/804d15f1-f18f-4397-9eae-8baf444b6e03" width="400" height="150"/>
    </div>
    <br>
     장점 : 연결 리스트를 사용하기 때문에 보다 유연하고, 해시 값을 그대로 사용할 수 있다. <br>
     한계점 : 연결 리스트를 사용한다는 것은 추가적인 공간이 필요하다는 의미이고, 연속된 데이터가 아니기 때문에 캐시의 도움을 받기 어렵다.

   <br>
   <br>

3. **개방 주소법(Open Addressing)** : 충돌이 발생하면 다른 해시 코드(버킷)를 사용하는 방법
   <div>
     <img src="https://github.com/yejinsohn/TIL/assets/104317217/b9876287-7a93-4dec-92b1-d9b7382e3635" width="300" height="170"/>
   </div> 
   <br>
    ➡️ 새로운 공간을 할당하는 대표적인 방법들 <br>
    - 선형 탐색(Linear Probing) : 충돌 시 다음 버킷, 혹은 몇 개의 버킷을 건너뛰어 데이터를 삽입<br>
    - 제곱 탐색(Quadratic Probing) : 충돌 시 제곱만큼 건너뛴 버킷에 데이터를 삽입(1,4,9,16..)<br>
    - 이중 해시(Double Hashing) : 충돌 시 다른 해시 함수를 한 번 더 적용한 결과를 이용<br>
    <br>
     장점 : 고정된 크기의 배열을 사용하기 때문에 데이터가 적을 때는 분리 연결법보다 좋은 성능을 가진다. <br>
     한계점 : 데이터가 많아지면 캐시에서 찾는 값을 꺼내 올 확률이 줄어들어 좋은 성능을 기대할 수 없다. 
