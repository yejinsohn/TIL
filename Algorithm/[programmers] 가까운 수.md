## 📍 Lv.0 가까운 수 <br>

#### 문제 <br>
<img src="https://github.com/yejinsohn/TIL/assets/104317217/da45e382-b2b4-476c-968a-0b175a7db3e1" width="470" height="290"/>

#### 내 코드 <br>

```Java
import java.util.*;

class Solution {
    public int solution(int[] array, int n) {
        int answer = 0;
        
        List<Integer> a = new ArrayList<>();
        
        Arrays.sort(array); // 배열 오름차순 정렬
        
        //배열의 원소에서 정수 n을 뺀 절대값 저장
        for (int i=0; i<array.length; i++) {
            a.add(Math.abs(array[i]-n));
        }
        // ArrayList에서 최소값을 구하고, 최소값의 인덱스를 저장
        int min = a.get(0); int idx = 0;
        for (int i=1; i<a.size(); i++) {
            if (a.get(i)<min) {
                min = a.get(i);
                idx = i;
            }
        } 
        answer = array[idx];
        return answer;
    }
}
```

##### 🌿 ArrayList를 활용해 문제를 풀 수 있었다!
