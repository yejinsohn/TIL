## 📍 Lv.0 배열 자르기 <br>

#### 문제 <br>
<img src="https://github.com/yejinsohn/TIL/assets/104317217/52eff915-f409-4b93-a7b5-51a406d473c9" width="490" height="470"/>

#### 내 코드 <br>

```Java
import java.util.Arrays;

class Solution {
    public int[] solution(int[] numbers, int num1, int num2) {
        
        return Arrays.copyOfRange(numbers,num1,num2+1); 
    }
}
```

##### 🌿 반복문 대신 Arrays 클래스의 메소드를 활용해 더욱 간단하게 풀 수 있었다!
