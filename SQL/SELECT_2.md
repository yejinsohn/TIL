## 📍 [programmers] 인기있는 아이스크림 <br>

#### 문제 <br>
<img src="https://github.com/yejinsohn/TIL/assets/104317217/69afa7eb-185c-416b-a362-c5b67235d14b" width="420" height="250"/>
<img src="https://github.com/yejinsohn/TIL/assets/104317217/13bb5ad8-1510-41ef-95ff-f6f8670c8f73" width="430" height="130"/>

#### 내 코드 <br>

```sql
SELECT FLAVOR
FROM FIRST_HALF
ORDER BY TOTAL_ORDER DESC, SHIPMENT_ID; // 총주문량을 기준으로 내림차순, 총주문량이 같을 경우 출하 번호를 기준으로 오름차순
```

##### 🌿 쉽게 풀 수 있었다!
