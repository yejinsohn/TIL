## 📍 Lv.0 각도기 <br>

#### 문제 <br>
<img src="https://github.com/yejinsohn/TIL/assets/104317217/90b8990f-1998-43c6-a7f7-aa8421913292" width="470" height="500"/>

#### 내 코드 <br>

```Java
class Solution {
    public int solution(int angle) {
        int answer = 0;
        
        if(angle==180){
            answer = 4;
        }
        else if(angle>90){
            answer = 3;
        }
        else if(angle==90){
            answer = 2;
        }
        else{
            answer = 1;  
         }
           
        return answer;
    }
}
```

##### 🌿 쉽게 풀 수 있었다!
