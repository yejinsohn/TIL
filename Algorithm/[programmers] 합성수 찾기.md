## 📍 Lv.0 합성수 찾기 <br>

#### 문제 <br>
<img src="https://github.com/yejinsohn/TIL/assets/104317217/c02156cb-4e21-43e6-8c78-1026eab7dab9" width="450" height="400"/>

#### 내 코드 <br>

```Java
class Solution {
    public int solution(int n) {
        int answer = 0;
        
        for(int i=1; i<=n; i++){
            int count = 0;
            for(int j=1; j<=i; j++){
                if(i%j==0){
                    count++;                
                }
            }
            if(count>=3){
                answer++;
            }
        }
        return answer;
    }
}
```

##### 🌿 count의 위치를 실수해 조금 헤맸지만, 쉽게 풀 수 있었다!
