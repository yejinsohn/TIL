## 📍 Lv.0 중복된 숫자 개수 <br>

#### 문제 <br>
<img src="https://github.com/yejinsohn/TIL/assets/104317217/e3ad5ac1-c9a1-437a-87e7-8d842b2354d8" width="470" height="470"/>

#### 내 코드 <br>

```Java
class Solution {
    public int solution(int[] array, int n) {
        int answer = 0;

        for(int i=0; i<array.length; i++){
            if(array[i] == n){
                answer++;
            }
        }
        return answer;
    }
}
```

##### 🌿 쉽게 풀 수 있었다!
