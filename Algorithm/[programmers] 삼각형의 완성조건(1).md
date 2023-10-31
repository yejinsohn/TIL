## 📍 Lv.0 삼각형의 완성조건(1) <br>

#### 문제 <br>
<img src="https://github.com/yejinsohn/TIL/assets/104317217/c1a86c13-a8b0-47c2-b23e-c35f1f98086a" width="450" height="370"/>

#### 내 코드 <br>

```Java
import java.util.*;

class Solution {
    public int solution(int[] sides) {
        int answer = 0;
        int sum = 0;
        Arrays.sort(sides); // 오름차순 정렬
        
        sum = sides[0] + sides[1];
        if(sides[2] < sum) {
            answer = 1;
        } else {
            answer = 2;
        }       
        return answer;
    }
}
```

##### 🌿 정렬을 이용해서 쉽게 풀 수 있었다!
