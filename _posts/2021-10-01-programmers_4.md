---
title: "[Level 1] 수박수박수박수박수박수?"
excerpt: "수박수박수박수박수박수?"

categories:
- 프로그래머스
tags:
- 코테
last_modified_at: 2021-10-01
---
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
