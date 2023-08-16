## 📍 Lv.0 문자열 정렬하기(1) <br>

#### 문제 <br>
<img src="https://github.com/yejinsohn/TIL/assets/104317217/0dcd8abf-8310-4a9b-ba21-006eca6f5abf" width="470" height="500"/>

#### 내 코드 <br>

```Java
import java.util.Arrays;

class Solution {
    public int[] solution(String my_string) {
        my_string = my_string.replaceAll("[a-z]","");
        
        String [] arr = my_string.split("");
        int [] answer = new int [arr.length];

        for(int i=0; i<arr.length; i++){
            answer[i] = Integer.parseInt(arr[i]);
        }
        
        Arrays.sort(answer);
        
        return answer;
    }
}
```

##### 🌿 쉽게 풀 수 있었다!
