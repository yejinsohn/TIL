## 💭 JPA(Java Persistence API)

JPA란 자바 진영에서 ORM(Object-Relational Mapping) 기술 표준으로 사용되는 인터페이스의 모음이다.<br>
즉, 실제로 구현된 것이 아니라 구현된 클래스와 매핑을 해주기 위해 사용되는 프레임워크를 의미한다.

> 여기서 ORM(Object-Relational Mapping)이란 우리가 일반적으로 알고 있는 애플리케이션 class와 RDB(Relational DataBase)의 테이블을 매핑해주는 기술로, 객체는 객체대로 생성하고, 데이터베이스는 데이터베이스에 맞도록 설계를 가능하게 해준다.

#### 동작 과정

<p align="center"><img src="https://github.com/yejinsohn/TIL/assets/104317217/232e9840-7c65-4fd6-9a73-21906034f2aa" width="600" height="200"/></p>

JPA는 애플리케이션과 JDBC(Java Database Connectivity) 사이에서 동작하며, JPA 내부에서 JDBC API를 사용하여 SQL을 호출하고 DB와 통신한다.
개발자가 ORM 프레임워크에 저장하면 적절한 INSERT SQL을 생성해 데이터베이스에 저장해주고, 검색을 하면 적절한 SELECT SQL을 생성해 결과를 객체에 매핑하고 전달해 준다.

#### 💡 왜 JPA를 사용해야 할까?
##### 1. 생산성 : 데이터베이스 중심이 아닌 객체 중심 개발 가능
##### 2. 유지보수 용이
##### 3. 패러다임의 불일치 해결
##### 4. 성능 최적화
##### 5. 데이터 접근 추상화와 벤더 독립성

------------

#### Spring Data JPA
Spring Data JPA는 JPA를 더 쉽게 사용하기 위해 Spring Data 프레임워크의 한 파트로 JPA를 이용한 구현체를 더 추상화시켜 더 쉽고 간편하게 JPA를 이용한 프로젝트를 개발할 수 있게 해주는 Spring 모듈이다. 
이러한 Spring Data JPA는 Hibernate와 같은 JPA구현체를 사용해서 JPA를 사용하게 된다. Spring Data JPA를 사용하면 사용자는 더욱 간단하게 데이터 접근이 가능해진다.

<p align="center"><img src="https://github.com/yejinsohn/TIL/assets/104317217/addec839-dd9d-4a1f-95d7-fdc68a3c52d0" width="500" height="380"/></p>

정리하자면, JPA는 자바 진영의 ORM 기술에 대한 API 표준 명세이며 Hibernate는 JPA의 구현체이고, 내부적으로 JDBC를 이용한다. <br>
Spring Data JPA는 JPA를 사용하기 쉽게 Spring에서 제공하는 모듈로 내부적으로 JPA 구현체를 이용한다.

------------

#### ddl-auto 옵션
##### 종류 <br>
- create: 기존 테이블 삭제 후 다시 생성 (DROP + CREATE)
- create-drop: create와 같으나 종료 시점에 테이블 DROP
- update: 변경만 반영 (운영DB에서는 사용하면 안됨)
- validate: Entity와 테이블이 정상 매핑되었는지만 확인
- none: 사용하지 않음 (사실상 없는 값)

##### 주의사항
create 옵션은 해당하는 테이블이 있으면 DROP하고 새로 만들어 버리기 때문에 ***로컬환경에서만*** 사용해야 한다! <br>
- 운영 장비에서는 crate, create-drop, update 사용 X
- 개발 초기 단계는 create 또는 update
- 테스트 서버는 update 또는 validate
- 스테이징과 운영 서버는 validate 또는 none
