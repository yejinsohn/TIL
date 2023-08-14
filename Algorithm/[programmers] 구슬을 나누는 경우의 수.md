## 📍 Lv.0 구슬을 나누는 경우의 수 <br>

#### 문제 <br>
<img src="https://github.com/yejinsohn/TIL/assets/104317217/bc9fb7d1-6793-445f-9e74-db41c77d6ac3" width="470" height="500"/>

#### 내 코드 <br>

```Java
class Solution {
    public int solution(int balls, int share) {
        return combination(balls, share);
    }

    public static int combination(int balls, int share) {
        if (balls == share || share == 0) return 1;
        return combination((balls-1), (share-1)) + combination(balls-1, share);
    }
}
```

##### 🌿 재귀함수를 이용해서 쉽게 풀 수 있었다!
