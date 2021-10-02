---
title: "[Level 1] 평균 구하기"
excerpt: "평균 구하기"

categories:
- 프로그래머스
tags:
- 코테
last_modified_at: 2021-10-01
---
```java
class Solution {
  public double solution(int[] arr) {
    double answer = 0;
    for (int i=0; i<arr.length; i++) {
      answer += arr[i];
    }
    answer = answer / arr.length;
    return answer;
  }
}
```
