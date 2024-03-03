## 📍 Lv.0 A로 B 만들기<br>

#### 문제 <br>
<img src="https://github.com/yejinsohn/TIL/assets/104317217/dcb1a70b-fe1b-4b70-8485-698baa1efdcb" width="470" height="230"/>

#### 내 코드 <br>

```Java
import java.util.*;

class Solution {
    public int solution(String before, String after) {
        int answer = 0;
        
        char [] before_char = before.toCharArray();
        char [] after_char = after.toCharArray();
        
        // 오름차순 정렬
        Arrays.sort(before_char);
        Arrays.sort(after_char);
        
        String str1 = new String(before_char);
        String str2 = new String(after_char);
        
        return str1.equals(str2) ? 1 : 0;
    }
}
```

##### 🌿 오름차순 정렬을 통해 쉽게 풀 수 있었다!
