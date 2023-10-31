## 📍 [programmers] 가격이 제일 비싼 식품의 정보 출력하기 <br>

#### 문제 <br>
<img src="https://github.com/yejinsohn/TIL/assets/104317217/bfce7e1a-aaa3-463a-8608-0ec51b21f87a" width="420" height="310"/>
<img src="https://github.com/yejinsohn/TIL/assets/104317217/fb620280-9668-4ae4-b440-c4ce5a31fa2c" width="430" height="100"/>

#### 내 코드 <br>

```sql
SELECT *
FROM FOOD_PRODUCT
ORDER BY PRICE DESC # 내림차순 정렬
LIMIT 1;
```

##### 🌿 쉽게 풀 수 있었다!
LIMIT : 데이터 조회 시 한계를 지정
