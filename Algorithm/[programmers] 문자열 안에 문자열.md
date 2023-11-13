## 📍 Lv.0 문자열 안에 문자열 <br>

#### 문제 <br>
<img src="https://github.com/yejinsohn/TIL/assets/104317217/b76a1feb-9c62-4a23-a638-1d0ec8f740a0" width="470" height="470"/>

#### 내 코드 <br>

```Java
class Solution {
    public int solution(String str1, String str2) {
        int answer = 0;

        if(str1.contains(str2)){
            answer = 1;
        } else {
            answer = 2;
        }
        return answer;
    }
}
```

##### 🌿 쉽게 풀 수 있었다!
