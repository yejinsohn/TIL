## 📍 Lv.0 n의 배수 고르기 <br>

#### 문제 <br>
<img src="https://github.com/yejinsohn/TIL/assets/104317217/fd2406a8-42a0-4fdf-8c55-1ed3c09d57e3" width="470" height="430"/>

#### 내 코드 <br>

```Java
class Solution {
    public int[] solution(int n, int[] numlist) {
        int count = 0; // n의 배수 개수
        
        for(int i=0; i<numlist.length; i++){
            if(numlist[i]%n == 0){ 
                count++;
            } 
        }
        
        int[] answer = new int[count]; // n의 배수로만 구성된 새로운 배열
        int j = 0;
        
         for(int i=0; i<numlist.length; i++){
            if(numlist[i]%n == 0){
                answer[j] = numlist[i];
                j++;
            } 
        }
        return answer;
    }
}
```

##### 🌿 쉽게 풀 수 있었다!
