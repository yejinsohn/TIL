## 📍 Lv.0 외계행성의 나이 <br>

#### 문제 <br>
<img src="https://github.com/yejinsohn/TIL/assets/104317217/279dd2ac-0805-4eb7-8f7f-0eb644fd55c1" width="490" height="500"/>

#### 내 코드 <br>

```Java
class Solution {
	public String solution(int age) {
      String answer = "";
      String age962 = "abcdefghij";
      String[] arr = String.valueOf(age).split("");
        
        for (int i = 0; i < arr.length; i++) {
        	answer += age962.charAt(Integer.valueOf(arr[i]));
		}
        return answer;
    }
}
```

##### 🌿 
