## BaekJoon/BOJ [JAVA] 설탕배달_2839

단계: 사칙연산 도전하기

HINT:
처음에는 DP로 풀어야하는건가 생각했었는데, 엄....뻘짓을 하다가, 규칙이 있다는 소리를 듣고 우선 나열을 해 보았다<br/>
3 &nbsp;&nbsp;&nbsp;&nbsp; 1 <br/>
4 &nbsp;&nbsp;&nbsp;&nbsp; -1 <br/>
~~<br/>
5&nbsp;&nbsp;&nbsp;&nbsp;1<br/>
6&nbsp;&nbsp;&nbsp;&nbsp;2<br/>
7&nbsp;&nbsp;&nbsp;&nbsp;-1<br/>
8&nbsp;&nbsp;&nbsp;&nbsp;2<br/>
9&nbsp;&nbsp;&nbsp;&nbsp;3<br/>
~~<br/>
10&nbsp;&nbsp;&nbsp;&nbsp;2<br/>
11&nbsp;&nbsp;&nbsp;&nbsp;3<br/>
12&nbsp;&nbsp;&nbsp;&nbsp;4<br/>
13&nbsp;&nbsp;&nbsp;&nbsp;3<br/>
14&nbsp;&nbsp;&nbsp;&nbsp;4<br/>
~~<br/>
15&nbsp;&nbsp;&nbsp;&nbsp;3<br/>
16&nbsp;&nbsp;&nbsp;&nbsp;4<br/>
17&nbsp;&nbsp;&nbsp;&nbsp;5<br/>
18&nbsp;&nbsp;&nbsp;&nbsp;4<br/>
19&nbsp;&nbsp;&nbsp;&nbsp;5<br/>
~~<br/>
20&nbsp;&nbsp;&nbsp;&nbsp;4<br/>
21&nbsp;&nbsp;&nbsp;&nbsp;5<br/>
.<br/>
.<br/>
.<br/>
규칙이 보인다. 규칙이 바로 이전 반복에서 1씩 증가는 것을 볼 수 있다. 극단적으로 하면 정말 극단적으로 할 수 있기에, 정말 그렇게 해보기로 했다. 난 간단한게 좋으니까!

```java

import java.util.*;
public class baekjoon_2839 {
    public static void main(String[] argc){
        Scanner scanner = new Scanner(System.in);
        int n = scanner.nextInt();
        int suger[] = {0,0,0,1,-1,1,2,-1,2,3,2,3,4,3,4};
        if(n<=9){
            System.out.println(suger[n]);
        }
        else {
            int tmp = n%5+10;
            System.out.println(suger[tmp]+n/5-2);
        }
    }
}
```
