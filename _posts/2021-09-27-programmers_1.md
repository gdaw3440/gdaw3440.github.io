---
title: "[Level 1] 음양 더하기"
excerpt: "음양 더하기"

categories:
- 프로그래머스
tags:
- 코테
last_modified_at: 2021-09-27
---

거진 한달 전, 인프런으로 코테 연습을 하다가 프로그래머스 주최 채용 코테를 풀게되었는데 익숙치가 않아 
그냥 프로그래머스에서 코테 연습을 하기로 하였다. 



문제 설명과 제한사항을 보자

> 문제 설명
> 
> 어떤 정수들이 있습니다. 이 정수들의 절댓값을 차례대로 담은 정수 배열 absolutes와 이 정수들의 부호를 차례대로 담은 불리언 배열 signs가 매개변수로 주어집니다. 실제 정수들의 합을 구하여 return 하도록 solution 함수를 완성해주세요.

> 제한 사항
> 
> signs[i] 가 참이면 absolutes[i] 의 실제 정수가 양수임을, 그렇지 않으면 음수임을 의미합니다.

요약하자면 absolutes에서는 숫자를, 불린형으로 받은 signs의 부호들을 매칭 후 각각 더해 리턴하면 되는 것

signs가 불린형이 아니였으면 더했을텐데, 불린형이라 매번 조건문으로 부호를 추가하기도 그래서 거짓일 경우(-일 경우) 빼고 참일 경우 더하는 형식으로 하였다.

오늘의 코테는 간단한 걸로 끝내기


```java
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



