## 📍 Lv.0 최댓값 만들기(1) <br>

#### 문제 <br>
<img src="https://github.com/yejinsohn/TIL/assets/104317217/2c45c410-2ba2-4e22-81ed-0c300e01070f" width="470" height="470"/>

#### 내 코드 <br>

```Java
class Solution {
    public int solution(int[] numbers) {
        int max = 0;

        for(int i=0; i<numbers.length; i++){
            for(int j=i+1; j<numbers.length; j++){
                if(numbers[i]*numbers[j]>max){
                    max = numbers[i]*numbers[j];
                }
            }
        }
        return max;
    }
}
```

##### 🌿 쉽게 풀 수 있었다!
