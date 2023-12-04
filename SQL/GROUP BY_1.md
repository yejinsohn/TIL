## 📍 [programmers] 자동차 종류 별 특정 옵션이 포함된 자동차 수 구하기 <br>

#### 문제 <br>
<img src="https://github.com/yejinsohn/TIL/assets/104317217/a71e8f11-61c6-44e9-a9fe-67367bb35349" width="420" height="380"/>
<img src="https://github.com/yejinsohn/TIL/assets/104317217/93817cc7-d692-4702-b1f3-281558a28beb" width="450" height="110"/>

#### 내 코드 <br>

```sql
SELECT CAR_TYPE, COUNT(*) AS CARS
FROM CAR_RENTAL_COMPANY_CAR
WHERE OPTIONS REGEXP '통풍시트|열선시트|가죽시트' # 정규식을 이용한 검색 방식
GROUP BY CAR_TYPE 
ORDER BY CAR_TYPE;
```

##### 🌿 쉽게 풀 수 있었다!
REGEXP는 LIKE를 이용한 검색과 달리 Regular Expression(정규 표현식)를 이용해 검색하기 때문에 기본 연산자보다 복잡한 문자열 조건을 걸어 데이터를 검색할 수 있다. <br>

정규 표현식 : 특정한 규칙을 가진 문자열의 집합을 표현하는데 사용하는 형식 언어 <br>
문자열을 처리하는 방법 중 하나로, 특정한 조건의 문자를 ‘검색’하거나 ‘치환’하는 과정을 매우 간편하게 처리할 수 있도록 해주는 수단
