## 📍 Lv.0 가장 큰 수 찾기 <br>

#### 문제 <br>
<img src="https://github.com/yejinsohn/TIL/assets/104317217/fd8b4843-e997-47a0-a7d6-7eb71841c5b0" width="470" height="420"/>

#### 내 코드 <br>

```Java
class Solution {
    public int[] solution(int[] array) {
        int[] answer = {0, 0};
        
        for(int i=0; i<array.length; i++){
            if(array[i] > answer[0]){
                answer[0] = array[i];
                answer[1] = i;
            }
        }
        return answer;
    }
}
```

##### 🌿 쉽게 풀 수 있었다!
