## 📍 Lv.0 순서쌍의 개수 <br>

#### 문제 <br>
<img src="https://github.com/yejinsohn/TIL/assets/104317217/b961f68e-7d48-485b-bc1d-485c503b4470" width="500" height="460"/>

#### 내 코드 <br>

```Java
class Solution {
    public int solution(int n) {
        int answer = 0;
        
        for(int i=1; i<=n; i++){
            if(n%i==0){
                answer ++;
            }
        }
        return answer;
    }
}
```

##### 🌿 쉽게 풀 수 있었다!
