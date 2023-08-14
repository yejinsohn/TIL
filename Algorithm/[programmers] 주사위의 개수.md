## 📍 Lv.0 주사위의 개수 <br>

#### 문제 <br>
<img src="https://github.com/yejinsohn/TIL/assets/104317217/d8bbe01e-c6a5-4300-a313-932e68140fed" width="470" height="500"/>

#### 내 코드 <br>

```Java
class Solution {
    public int solution(int[] box, int n) {
        int answer = 0;

        int a = box[0]/n;
        int b = box[1]/n;
        int c = box[2]/n;
        
        answer = a*b*c;
        
        return answer;
    }
}
```

##### 🌿 쉽게 풀 수 있었다!
