## 📍 [programmers] 평균 일일 대여 요금 구하기 <br>

#### 문제 <br>
<img src="https://github.com/yejinsohn/TIL/assets/104317217/7912319c-15d7-416e-b5cf-25a2cf135fe8" width="420" height="400"/>
<img src="https://github.com/yejinsohn/TIL/assets/104317217/60bcc24a-e02a-4763-9962-43bda60bc5eb" width="430" height="130"/>

#### 내 코드 <br>

```sql
SELECT ROUND(AVG(DAILY_FEE)) AS AVERAGE_FEE
FROM CAR_RENTAL_COMPANY_CAR
WHERE CAR_TYPE = 'SUV';
```

##### 🌿 쉽게 풀 수 있었다!
