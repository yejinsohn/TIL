## 📍 Lv.0 k의 개수 <br>

#### 문제 <br>
<img src="https://github.com/yejinsohn/TIL/assets/104317217/4e191d8b-3123-412b-8444-07b58a79d7dc" width="470" height="260"/>

#### 내 코드 <br>

```Java
class Solution {
    public int solution(int i, int j, int k) {
        int count = 0;

        // 문자열로 변환 후 비교
        String string_k = String.valueOf(k);
        for (int l = i; l <= j; l++) {
            String value = String.valueOf(l);
            if (value.contains(string_k)) {
                String[] array = value.split("");
                for (String alpha : array) {
                    if (alpha.equals(string_k)) {
                        count++;
                    }
                }
            }
        }
        return count;
    }
}
```

##### 🌿 쉽게 풀 수 있었다!
