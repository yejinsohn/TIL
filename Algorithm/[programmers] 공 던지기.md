## 📍 Lv.0 공 던지기 <br>

#### 문제 <br>
<img src="https://github.com/yejinsohn/TIL/assets/104317217/7580d9d6-fe1d-4b9a-bd0c-ff603ed55e12" width="470" height="400"/>

#### 내 코드 <br>

```Java
class Solution {
    public int solution(int[] numbers, int k) {
        int answer = numbers[2 * (k - 1) % numbers.length];
        return answer;
    }
}
```

##### 🌿 쉽게 풀 수 있었다!
