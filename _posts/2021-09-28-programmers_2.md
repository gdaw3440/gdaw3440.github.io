---
title: "[Level 1] 숫자 문자열과 영단어"
excerpt: "숫자 문자열과 영단어"

categories:
- 프로그래머스
tags:
- 코테
last_modified_at: 2021-09-28
---





이번 문제는 예시만 봐도 충분 할 듯 하다.

이중 포문을 돌려서 해야하나 싶었는데 replace가 정말 좋긴 한듯



> - 1478 → "one4seveneight"
> - 234567 → "23four5six7"
> - 10203 → "1zerotwozero3"




```java
class Solution {
    public int solution(String s) {
        int answer = 0;
        String[] num = {"0", "1", "2", "3", "4", "5", "6", "7", "8", "9"}, 
                 str = {"zero", "one", "two", "three", "four", "five", "six", "seven", "eight", "nine"};
        for (int i=0; i<10; i++) {
            s = s.replace(str[i], num[i]);
        }
        answer = Integer.parseInt(s);
        return answer;
    }
}
```

