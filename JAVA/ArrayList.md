## 💭 ArrayList란?
ArrayList는 배열을 기반으로 하는 컬렉션 중 하나로, 한번 생성하면 크기가 고정되는 배열과 다르게 부족한 공간을 자동으로 늘려주는 '선형리스트'다. <br>
ArrayList를 생성하게 되면 내부에서는 데이터를 저장하기 위한 초기 용량(Capacity) 크기의 저장공간이 할당되며, 데이터의 크기가 초기 용량의 크기를 넘어서게 되면 저장 공간이 새롭게 할당된다. 

<img src="https://github.com/yejinsohn/TIL/assets/104317217/3099219d-04a0-400a-b019-5f20640110e8" width="500" height="300"/>

### 📍 특징
- 연속적인 데이터 리스트다. (중간에 빈 공간 X) <br>
- ArrayList 클래스는 내부적으로 Object[] 배열을 이용하여 요소를 저장한다. <br>
- 인덱스를 이용해 각 요소에 빠르게 접근이 가능하다. <br>
- 크기가 고정되어있는 배열과 달리 데이터 적재량에 따라 가변적으로 공간을 늘리거나 줄인다. (배열 공간이 꽉 차면 배열을 copy하는 방식으로 늘리므로 이 과정에서 지연이 발생) <br>
- 데이터를 리스트 중간에 삽입/삭제 할 경우, 중간에 빈 공간이 생기지 않도록 요소들의 위치를 앞뒤로 자동으로 이동시키기 때문에 삽입/삭제 동작은 느리다. <br>
- capacity는 리스트의 공간 용량, size는 리스트 안에 들어있는 요소들의 총 개수를 의미한다.

### 📙 ArrayList 생성
```Java
// 타입 설정
ArrayList<Integer> list1 = new ArrayList<>();

// 초기 용량(capacity)지정
ArrayList<Integer> list2 = new ArrayList<>(10);

// 배열을 넣어 생성
ArrayList<Integer> list3 = new ArrayList<>(Arrays.asList(1,2,3));

// 다른 컬렉션으로부터 그대로 요소를 받아와 생성 (ArrayList를 인자로 받는 API를 사용하기 위해서 Collection 타입 변환이 필요할 때 많이 사용)
ArrayList<Integer> list4 = new ArrayList<>(list3);
```

### 📙 ArrayList 데이터 추가
🔔 ArrayList에 요소를 추가할 때, 제네릭 타입 파라미터로 명시된 타입의 데이터만 추가 가능!

✔️ add()를 이용한 추가 
```Java
// ArrayList의 마지막에 객체를 추가
ArrayList<String> list1 = new ArrayList<>();

list1.add("A");
list1.add("B");
list1.add("C");

System.out.println(list1); // [A, B, C]
```

✔️ addAll()를 이용한 추가
```Java
// 컬렉션 자체를 추가
ArrayList<String> list1 = new ArrayList<>();
list1.add("1");
list1.add("2");

ArrayList<String> list2 = new ArrayList<>();
list2.add("3");
list2.add("4");

list1.addAll(list2); // list1에 list2의 내용을 추가한다.
 
System.out.println(list1); // [1, 2, 3, 4]
```

### 📙 ArrayList 데이터 삽입
🔔 추가하는 요소의 위치 지정하면 기존 데이터는 뒤로 밀려난다!

✔️ add()를 이용한 삽입
```Java
ArrayList<String> list1 = new ArrayList<>(); 

list1.add("1");
list1.add("2");
list1.add("3");
list1.add("4");
list1.add("5");

// 3번째 인덱스 자리에 요소 삽입
list1.add(3, "A");

System.out.println(list1); // [1, 2, 3, A, 4, 5]
```

❗️데이터 삽입 주의사항 (IndexOutOfBoundsException) <br>
데이터의 위치를 지정하여 삽입할 때 인덱스가 리스트의 capacity를 넘지 않도록 주의해야 한다.<br>
리스트의 용량보다 큰 인덱스로 데이터를 삽입하게 되면 당연히 에러가 발생한다. <br>
<br>
또한, 인덱스가 리스트의 용량에 맞춰 적재된 요소의 마지막 위치(size 값)에서 벗어나도 IndexOutOfBoundsException이 발생한다. <br>
ArrayList는 '데이터가 연속된 자료구조'라는 규칙이 정해져 있기 때문에 데이터들 사이에 빈 공간이 존재하면 안되기 때문이다. <br>
예를 들어, [1, 2, 3, 4, 5]가 저장되어 있는 리스트의 7번째 인덱스에 'A'라는 데이터를 추가하는 것은 리스트의 물리적인 공간의 크기(capacity)는 충분하더라도 논리적인 공간(size)은 5이기 때문에 7번째 공간에 값을 삽입하는 것은 불가능하다. 

### 📙 ArrayList 데이터 삭제
🔔 리스트의 중간에 위치한 데이터를 삭제하면 나머지 요소들이 빈 공간을 채우기 위해 앞 쪽으로 이동한다!

✔️ remove(), clear()
```Java
ArrayList<String> list1 = new ArrayList<>(); 

list1.add("1");
list1.add("2");
list1.add("3");
list1.add("4");
list1.add("5");

// 2번째 인덱스 자리의 요소 삭제
list1.remove(2);

System.out.println(list); // [1, 2, 4, 5]

list1.clear(); // list1의 데이터를 모두 비운다.

System.out.println(list1); // []
```

### 📙 ArrayList 데이터 검섹

✔️ contains(), indexOf(), lastIndexOf()
```Java
ArrayList<String> list1 = new ArrayList<>();
list1.add("A");
list1.add("B");
list1.add("C");
list1.add("D");

// list에 A가 있는지 검색 
list1.contains("A"); // true

// list에 D가 있는지 순차적으로 검색하고 index를 반환 (없으면 -1)
list1.indexOf("A"); // 0

// list에 D가 있는지 연순으로 검색하고 index를 반환 (만일 없으면 -1)
list1.lastIndexOf("D"); // 3
```
