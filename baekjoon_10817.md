## BaekJoon/BOJ [JAVA] 세 수_10817

HINT: 3개 뿐이 안되니까 기본 sort를 사용하자! Collections.sort()이다.

```java

import java.util.ArrayList;
import java.util.Collections;
import java.util.Scanner;
public class baekjoon_10817 {
    public static void main(String[] argc){
        Scanner scanner = new Scanner(System.in);
        ArrayList<Integer> num = new ArrayList<>();
        for(int i=0;i<3;i++) num.add(Integer.parseInt(scanner.next()));
        Collections.sort(num);
        System.out.println(num.get(1));
    }
}


```
