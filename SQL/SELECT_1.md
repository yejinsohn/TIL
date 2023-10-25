## 📍 [programmers] 12세 이하인 여자 환자 목록 출력하기 <br>

#### 문제 <br>
<img src="https://github.com/yejinsohn/TIL/assets/104317217/224042f2-ca7b-47bf-9992-20a2a30208ad" width="420" height="300"/>
<img src="https://github.com/yejinsohn/TIL/assets/104317217/0ab6b68f-dadb-4773-979d-f12a2ce76c3c" width="450" height="180"/>

#### 내 코드 <br>

```sql
SELECT PT_NAME, PT_NO, GEND_CD, AGE, COALESCE(TLNO, 'NONE') AS TLNO // 전화번호가 없는 경우, 'NONE'으로 출력
FROM PATIENT
WHERE AGE <= 12 AND GEND_CD = 'W'  // 12세 이하인 여자
ORDER BY AGE DESC, PT_NAME; // 나이를 기준으로 내림차순, 나이가 같을 경우 환자 이름을 기준으로 오름차순
```

##### 🌿 전화번호가 없는 경우(Null), 'NONE'으로 출력시켜주기 위해 COALESCE() 함수를 사용해줬다. <br>
COALESCE() : 인자로 주어진 컬럼들 중에서 NULL이 아닌 첫 번째 값을 반환하는 함수 <br>
조건에 따라서 두 칼럼을 합치는 기능 -> NULL 값을 특정 값으로 변환하는 데 사용할 수 있다! 
