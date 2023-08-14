## 📍 Lv.0 개미군단 <br>

#### 문제 <br>
<img src="https://github.com/yejinsohn/TIL/assets/104317217/1215f207-56a9-4b4a-9e3b-45157ec0fc94" width="470" height="500"/>

#### 내 코드 <br>

```Java
class Solution {
    public int solution(int hp) {
        int answer = 0;

        answer += hp/5;
        hp = hp%5;
        
        answer += hp/3;
        hp = hp%3;
        
        answer += hp/1;
        
        return answer;
    }
}
```

##### 🌿 쉽게 풀 수 있었다!
