## 📍 Lv.0 양꼬치 <br>

#### 문제 <br>
<img src="https://github.com/yejinsohn/TIL/assets/104317217/8b567e06-6bc8-42f7-8f29-678c753e4d3d" width="400" height="420"/>

#### 내 코드 <br>

```Java
class Solution {
    public int solution(int n, int k) {
        int answer = 0;
        int b;  // 서비스로 받은 음료수의 개수
        
        if(n>=10){
            b = n/10; // 10인분당 1개의 서비스 음료
            answer = (12000*n) + (2000*(k-b));
        }else{
            answer = (12000*n) + (2000*k);
        }
        
        return answer;
    }
}
```

##### 🌿 쉽게 풀 수 있었다!
