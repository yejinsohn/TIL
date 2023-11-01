## 📍 Lv.0 자릿수 더하기 <br>

#### 문제 <br>
<img src="https://github.com/yejinsohn/TIL/assets/104317217/202f4197-6e29-45fc-bc16-156fa77c96c4" width="470" height="400"/>

#### 내 코드 <br>

```Java
class Solution {
    public int solution(int n) {
        int answer = 0;
        
        while(n > 0){
            answer += n%10;
            n = n/10;
        }
        return answer;
    }
}
```

##### 🌿 쉽게 풀 수 있었다!
