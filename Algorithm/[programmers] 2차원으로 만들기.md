## 📍 Lv.0 2차원으로 만들기 <br>

#### 문제 <br>
<img src="https://github.com/yejinsohn/TIL/assets/104317217/9062fec2-8ae4-49b1-8f43-b3f51a0dc3d3" width="470" height="500"/>

#### 내 코드 <br>

```Java
class Solution {
    public int[][] solution(int[] num_list, int n) {
        int[][] answer = new int[num_list.length/n][n];
        int index = 0;

        for(int i=0; i<num_list.length/n; i++){
            for(int j=0; j<n; j++){
                answer [i][j] = num_list[index];
                index++;
            }
        }
        return answer;
    }
}
```

##### 🌿 쉽게 풀 수 있었다!
