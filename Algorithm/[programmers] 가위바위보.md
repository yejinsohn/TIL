## 📍 Lv.0 가위바위보 <br>

#### 문제 <br>
<img src="https://github.com/yejinsohn/TIL/assets/104317217/80cc095d-7692-4bb7-a324-5cda1d81f55a" width="470" height="500"/>

#### 내 코드 <br>

```Java
class Solution {
    public String solution(String rsp) {
        String answer = "";
        String [] arr = rsp.split("");

        for(int i=0; i<arr.length; i++){
            if(arr[i].equals("2"))
                answer += "0";
            else if(arr[i].equals("0"))
                answer += "5";
            else
                answer += "2";
        }
        return answer;
    }
}
```

##### 🌿 쉽게 풀 수 있었다!
