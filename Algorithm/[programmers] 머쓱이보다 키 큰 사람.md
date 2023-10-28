## 📍 Lv.0 머쓱이보다 키 큰 사람 <br>

#### 문제 <br>
<img src="https://github.com/yejinsohn/TIL/assets/104317217/d47df6ac-4d8f-4a5d-bf7c-4216a2d6b5f1" width="470" height="370"/>

#### 내 코드 <br>

```Java
class Solution {
    public int solution(int[] array, int height) {
        int answer = 0; // 키 큰 사람 수
        
        for(int i=0; i < array.length; i++){
            if(array[i] > height){
                answer ++;
            }
        return answer;
    }
}
```

##### 🌿 쉽게 풀 수 있었다!
