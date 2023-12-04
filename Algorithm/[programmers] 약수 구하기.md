## 📍 Lv.0 약수 구하기 <br>

#### 문제 <br>
<img src="https://github.com/yejinsohn/TIL/assets/104317217/58b8b24a-d473-4708-98b1-d04177095c8a" width="470" height="340"/>

#### 내 코드 <br>

```Java
import java.util.*;

class Solution {
    public int[] solution(int n) {
        int count = 0; // 배열 크기
        int a = 0; 
        
        for(int i=1; i<=n; i++){
            if(n%i == 0){
                count++;
            }
        }
        
        int [] answer = new int [count];

        for(int i=1; i<=n; i++){
            if(n%i == 0){
                answer[a] = i;
                a++;
            }
        }
        
        Arrays.sort(answer);
        return answer;
    }
}
```

##### 🌿 쉽게 풀 수 있었다!
