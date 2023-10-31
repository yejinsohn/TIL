## 📍 Lv.0 제곱수 판별하기 <br>

#### 문제 <br>
<img src="https://github.com/yejinsohn/TIL/assets/104317217/c805f4b1-2959-466d-923c-e025a63acf29" width="450" height="300"/>

#### 내 코드 <br>

```Java
class Solution {
    public int solution(int n) {
        int answer = 0;
        
        if(Math.sqrt(n) % 1 == 0){ // 제곱근이 존재할 때
            answer = 1;
        } else {
            answer = 2;
        }
        return answer;
    }
}
```

##### 🌿 java.lang.Math 클래스의 sqrt()메소드를 이용해 쉽게 풀 수 있었다!
Math.pow(n, a) : n의 a승 반환 <br>
Math.sqrt(n) : n의 제곱근 반환
