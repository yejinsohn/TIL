## 📍 Lv.0 점의 위치 구하기 <br>

#### 문제 <br>
<img src="https://github.com/yejinsohn/TIL/assets/104317217/64d06cf3-5d15-4f1d-9317-b70b0d7ff15a" width="470" height="500"/>
<img src="https://github.com/yejinsohn/TIL/assets/104317217/613d2251-1156-4d63-ab3f-29d7cdc30db6" width="470" height="400"/>

#### 내 코드 <br>

```Java
class Solution {
    public int solution(int[] dot) {
        int answer = 0;
        
            if(dot[0]>0 && dot[1]>0){
                 answer = 1;
            }
            else if(dot[0]<0 && dot[1]>0){
                 answer = 2;
            }
            else if(dot[0]<0 && dot[1]<0){
                 answer = 3;
            }
            else{
                 answer = 4;
            }
        return answer;
    }
}
```

##### 🌿 쉽게 풀 수 있었다!
