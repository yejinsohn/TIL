## 📍 Lv.0 중복된 문자 제거 <br>

#### 문제 <br>
<img src="https://github.com/yejinsohn/TIL/assets/104317217/1a0a4ba6-331d-424e-baac-0891f188870a" width="470" height="330"/>

#### 내 코드 <br>

```Java
class Solution {
    public String solution(String my_string) {
        String answer = "";
        
        for(int i=0; i<my_string.length(); i++){
            if(my_string.indexOf(my_string.charAt(i)) == i){
                answer += my_string.charAt(i);
            }
        }
        return answer;
    }
}
```

##### 🌿 쉽게 풀 수 있었다!
