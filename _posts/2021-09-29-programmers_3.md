---
title: "[Level 1] 내적
excerpt: "내적"

categories:
- 프로그래머스
tags:
- 코테
last_modified_at: 2021-09-29
---





이번 문제는 예시만 봐도 충분 할 듯 하다.

그냥 곱하는 걸로 마무리

>  | a           | b             | result |
>   | ----------- | ------------- | ------ |
>   | `[1,2,3,4]` | `[-3,-1,0,2]` | 3      |
>   | `[-1,0,1]`  | `[1,0,-1]`    | -2     |
>




```java
class Solution {
    public int solution(int[] a, int[] b) {
        int answer = 0;
        for(int i=0; i<=a.length-1; i++){
            answer += a[i] * b[i];
        }
        return answer;   
    }
}
```

