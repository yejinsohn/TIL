## 📍 Lv.0 모스부호(1) <br>

#### 문제 <br>
<img src="https://github.com/yejinsohn/TIL/assets/104317217/5c435db1-9a5f-444f-b32a-52dc81aaa84a" width="470" height="500"/>

#### 내 코드 <br>

```Java
class Solution {
    public String solution(String letter) {
        String[] morse = {".-","-...","-.-.","-..",".","..-.",
                "--.","....","..",".---","-.-",".-..","--","-.",
                "---",".--.","--.-",".-.","...","-","..-","...-",
                ".--","-..-","-.--","--.."};
        
        String[] morseString;
        morseString = letter.split(" ");

        StringBuilder sb = new StringBuilder();
        for (String s : morseString) {
            for (int i = 0; i < morse.length; i++) {
                if (s.equals(morse[i])) sb.append(Character.toString(i + 'a'));
            }
        }
        return sb.toString();
    }
}
```

##### 🌿 'a' 대신 아스키 코드인 97을 넣어도 가능하다!
