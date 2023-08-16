## 📍 Lv.0 소인수분해 <br>

#### 문제 <br>
<img src="https://github.com/yejinsohn/TIL/assets/104317217/451055f9-6932-4634-8b72-1c502b2a7be3" width="460" height="450"/>

#### 내 코드 <br>

```Java
import java.util.*;

class Solution {
    public int[] solution(int n) {
        ArrayList<Integer> list = new ArrayList<>();
        
        for(int i=2; i<=n; i++){
            if(n%i ==0){
               while(n%i == 0){
                  n /= i;   
                }
                list.add(i);
            }
        }

        int [] answer = new int [list.size()];
        
        for(int i=0; i<answer.length; i++){
            answer[i] = list.get(i);
        }
        return answer;
    }
}
```

##### 🌿 쉽게 풀 수 있었다!
