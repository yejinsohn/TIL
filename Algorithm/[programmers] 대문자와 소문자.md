## 📍 Lv.0 대문자와 소문자 <br>

#### 문제 <br>
<img src="https://github.com/yejinsohn/TIL/assets/104317217/676299e3-5978-41c2-92dd-76220bec3121" width="470" height="420"/>

#### 내 코드 <br>

```Java
class Solution {
  public String solution(String my_string) {
    String answer = "";
    char [] array = my_string.toCharArray();
		
    // 아스키코드
    // a ~ z 97 ~122 
    // A ~ Z 65~90
		
    String temp ="";

    for(int i = 0; i<array.length; i++) {
      if(array[i] >= 97 && array[i] <= 122) {
        temp = array[i] + "";
        answer += temp.toUpperCase();
      }
      else if(array[i] >=65 && array[i] <= 90) {
        temp = array[i] + "";
        answer += temp.toLowerCase();
      }
    }
    return answer;
    }
}
```

##### 🌿 아스키 코드를 이용해 쉽게 풀 수 있었다!
