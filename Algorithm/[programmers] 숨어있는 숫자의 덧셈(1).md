## 📍 Lv.0 숨어있는 숫자의 덧셈(1) <br>

#### 문제 <br>
<img src="https://github.com/yejinsohn/TIL/assets/104317217/2ace97a5-2905-46a3-885c-4ff4b6330f32" width="480" height="460"/>

#### 내 코드 <br>

```Java
class Solution {
    public int solution(String my_string) {
        my_string = my_string.replaceAll("[a-zA-Z]", "");
        String [] arr = my_string.split("");
                
        int answer = 0;
        for (int i = 0; i < arr.length; i++) {
			answer += Integer.valueOf(arr[i]); 
		}
        return answer;
    }
}
```

##### 🌿 쉽게 풀 수 있었다!
