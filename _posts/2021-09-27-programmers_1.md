---
title: "[프로그래머스]음양 더하기"
excerpt: "1.음양 더하기"

categories:
- 프로그래머스
tags:
- 코테
last_modified_at: 2021-09-27
---

거진 한달 전, 인프런으로 코테 연습을 하다가 프로그래머스 주최 채용 코테를 풀게되었는데 익숙치가 않아 

그냥 프로그래머스에서 코테 연습을 하기로 오늘 마음을 먹었다.
 


absolutes에서는 숫자를, signs에서는 부호를 불린으로 받아서 세 수의 합을 리턴하면 되는 것

signs가 불린형이 아니였으면 더했을텐데, 불린형이라 매번 조건문으로 부호를 추가하기도 그래서 거짓일 경우(-일 경우) 빼고 참일 경우 더하는 형식으로 하였다.

오늘의 코테 끝


```
class Solution {
    public int solution(int[] absolutes, boolean[] signs) {
        int answer = 0;
        for (int i=0; i<signs.length; i++) {
            if(signs[i] != true) {
                answer -= absolutes[i];
            } else {
                answer += absolutes[i];
            }
        }
        return answer;        
    }
}
```




