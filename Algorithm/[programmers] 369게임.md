## 📍 Lv.0 369게임 <br>

#### 문제 <br>
<img src="https://github.com/yejinsohn/TIL/assets/104317217/bc2d74d8-2f53-4bfa-b17f-8c18231a1973" width="470" height="250"/>

#### 내 코드 <br>

```Java
class Solution {
    public int solution(int order) {
        int answer = 0;
        
        String order_str = Integer.toString(order);
        String [] array = order_str.split("");
        
        for (int i = 0; i < array.length; i++) {
            if (array[i].equals("3") || array[i].equals("6") || array[i].equals("9")) {
                answer++;
            }
        }
        return answer;
    }
}
```

##### 🌿 쉽게 풀 수 있었다!
