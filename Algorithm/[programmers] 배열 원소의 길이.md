## 📍 Lv.0 배열 원소의 길이 <br>

#### 문제 <br>
<img src="https://github.com/yejinsohn/TIL/assets/104317217/68558085-7e3d-46d9-9485-8b5552d626d6" width="470" height="300"/>

#### 내 코드 <br>

```Java
class Solution {
    public int[] solution(String[] strlist) {
        int [] answer = new int[strlist.length];
        
        for(int i=0; i<strlist.length; i++){
                answer[i] = strlist[i].length();
        }      
        return answer;
    }
}
```

##### 🌿 쉽게 풀 수 있었다!
