## 📍 Lv.0 진료 순서 정하기 <br>

#### 문제 <br>
<img src="https://github.com/yejinsohn/TIL/assets/104317217/ccebb14e-2955-4e57-81bf-1fac6c6e58e8" width="490" height="480"/>

#### 내 코드 <br>

```Java
class Solution {
    public int[] solution(int[] emergency) {
        int[] answer = new int [emergency.length];
        
        for(int i=0; i<emergency.length; i++){
            for(int j=0; j<emergency.length; j++){
                if(emergency[i] <= emergency[j]){
                    answer[i] ++;
                }
            }   
        }
        return answer;
    }
}
```

##### 🌿 쉽게 풀 수 있었다!
