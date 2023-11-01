## 📍 Lv.0 배열의 유사도 <br>

#### 문제 <br>
<img src="https://github.com/yejinsohn/TIL/assets/104317217/ab5f8c82-9758-4b46-82f3-88e6b34ab6d2" width="470" height="490"/>

#### 내 코드 <br>

```Java
class Solution {
    public int solution(String[] s1, String[] s2) {
        int answer = 0;
        
        for(int i=0; i<s1.length; i++){
            for(int j=0; j<s2.length; j++){
                if(s1[i].equals(s2[j])){ // 문자 비교
                    answer++;
                }
            }
        }
        return answer;
    }
}
```

##### 🌿 쉽게 풀 수 있었다!
