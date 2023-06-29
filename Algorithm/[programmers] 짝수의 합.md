## 📍 Lv.0 짝수의 합 <br>

#### 문제 <br>
<img src="https://github.com/yejinsohn/TIL/assets/104317217/f8b631e2-b3b3-4400-84b5-d45e91ecce11" width="400" height="370"/>

#### 내 코드 <br>

```Java
class Solution {
    public int solution(int n) {
        int answer = 0;

        for(int i=0; i<=n; i++){
            if(i%2==0){
                answer += i;
            }
        } 
        
        return answer;
    }
}
```

##### 🌿 쉽게 풀 수 있었다!
