## 📍 Lv.0 암호 해독 <br>

#### 문제 <br>
<img src="https://github.com/yejinsohn/TIL/assets/104317217/a098d554-2dcd-4020-af8a-465e5417a186" width="470" height="500"/>

#### 내 코드 <br>

```Java
class Solution {
    public String solution(String cipher, int code) {
        String answer = "";
        String [] s = cipher.split("");
        
        for(int i = 0; i < s.length; i++){
            if((i+1)%code == 0){
                answer += s[i];
            };
            
        }
        return answer;
    }
}
```

##### 🌿 쉽게 풀 수 있었다!
