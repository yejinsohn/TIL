## 📍 Lv.0 팩토리얼 <br>

#### 문제 <br>
<img src="https://github.com/yejinsohn/TIL/assets/104317217/4243fa83-8803-42c5-8935-92fbd533da99" width="470" height="470"/>

#### 내 코드 <br>

```Java
class Solution {
    public int solution(int n) {
        int answer = 0;
        
        for(int i=1; i<=10; i++){
            if(n>=factorial(i)){
                answer = i;
            }else{
                break;
            }
        }
        return answer;
    }

    public static int factorial(int number){
        if(number>1){
            number *= factorial(number-1);
        }
        return number;
    }
}
```

##### 🌿 쉽게 풀 수 있었다!
