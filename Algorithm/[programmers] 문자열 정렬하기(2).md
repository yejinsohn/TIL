## 📍 Lv.0 문자열 정렬하기(2) <br>

#### 문제 <br>
<img src="https://github.com/yejinsohn/TIL/assets/104317217/4820e229-7892-4cf8-8037-a5683d6055d9" width="470" height="240"/>

#### 내 코드 <br>

```Java
import java.util.*;

class Solution {
    public String solution(String my_string) {
        my_string = my_string.toLowerCase(); // 소문자 변환
        
        char [] array = my_string.toCharArray();
        Arrays.sort(array); // 순서 정렬
        
        String answer = new String(array);
        return answer;
    }
}
```

##### 🌿 쉽게 풀 수 있었다!
