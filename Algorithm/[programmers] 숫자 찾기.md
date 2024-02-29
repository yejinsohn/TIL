## 📍 Lv.0 숫자 찾기 <br>

#### 문제 <br>
<img src="https://github.com/yejinsohn/TIL/assets/104317217/11bb0e3a-2e9f-4371-9358-49cd7db9a7c7" width="470" height="270"/>

#### 내 코드 <br>

```Java
class Solution {
    public int solution(int num, int k) {
        String num_str = Integer.toString(num);
        String [] array = num_str.split("");
        
        for (int i = 0; i < array.length; i++) {
            if (array[i].equals(Integer.toString(k))) {
                return i+1;
            }
        }
        return -1;
    }
}
```

##### 🌿 쉽게 풀 수 있었다!
