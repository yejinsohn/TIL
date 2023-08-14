## 📍 Lv.0 배열 회전시키기 <br>

#### 문제 <br>
<img src="https://github.com/yejinsohn/TIL/assets/104317217/2a4c8e6e-2d68-45f1-a913-c80274b3b332" width="470" height="450"/>

#### 내 코드 <br>

```Java
class Solution {
    public int[] solution(int[] numbers, String direction) {

        if (direction.equals("right")) {
            int temp = numbers[numbers.length - 1];
            for (int i = numbers.length - 2; i >= 0; i--) {
                numbers[i + 1] = numbers[i];
            }
            numbers[0] = temp;
            return numbers;
        } else {
            int temp = numbers[0];
            for (int i = 0; i <= numbers.length - 2; i++) {
                numbers[i] = numbers[i + 1];
            }
            numbers[numbers.length - 1] = temp;
            
            return numbers;
        }
    }
}
```

##### 🌿 쉽게 풀 수 있었다!
