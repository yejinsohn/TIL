## 📍 Lv.0 최댓값 만들기(2) <br>

#### 문제 <br>
<img src="https://github.com/yejinsohn/TIL/assets/104317217/10ff08b7-ea68-4b40-9d40-aaf77b25ce69" width="470" height="420"/>

#### 내 코드 <br>

```Java
import java.util.*;

class Solution {
    public int solution(int[] numbers) {
        Arrays.sort(numbers); // 오름차순 정렬
        
        int answer1 = numbers[0] * numbers[1]; // 음수가 2개 이상 존재할 경우 최댓값
        int answer2 = numbers[numbers.length-1] * numbers[numbers.length-2]; // 양수 최댓값
        
        return answer1 > answer2 ? answer1 : answer2;  
    }
}
```


**🌿 쉽게 풀 수 있었다!** <br>

오름차순 정렬을 했을 때 음수가 2개 이상 존재할 경우, 음수 값 기준으로는 왼쪽 2개의 곱이 최댓값이 되고 양수 값 기준으로는 오른쪽 2개의 곱이 최댓값이 되므로
2가지 경우의 수를 비교해주었다.
