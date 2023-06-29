Lv.0 짝수의 합
<img src="https://github.com/yejinsohn/TIL/assets/104317217/a2db07e2-e07a-4965-b94a-c254b244e6b5" width="700" height="350"/>

내 코드
```Java
class Solution {
    public int solution(int n) {
        int answer = 0;
        
        for(int i=0; i<=n; i++){
            if(i%2==0){
                answer += i;
            }
        }
        
        return answer;
    }
}
```
