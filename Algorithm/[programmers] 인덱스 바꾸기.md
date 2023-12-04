## 📍 Lv.0 인덱스 바꾸기 <br>

#### 문제 <br>
<img src="https://github.com/yejinsohn/TIL/assets/104317217/31875f60-a238-4bdd-b0c5-1c42580b384c" width="470" height="500"/>

#### 내 코드 <br>

```Java
class Solution {
    public String solution(String my_string, int num1, int num2) {
        char [] answer = my_string.toCharArray();
        
        answer[num1] = my_string.charAt(num2);
        answer[num2] = my_string.charAt(num1);
        
        return String.valueOf(answer); // 객체를 String 문자열 참조 자료형으로 형 변환
    }
}
```

##### 🌿 쉽게 풀 수 있었다!
