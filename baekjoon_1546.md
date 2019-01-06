## BaekJoon/BOJ [JAVA] 평균_1546

HINT: 나눗셈 등에서 int형끼리의 계산이 되면 아무리 float로 해도 int로 저장이 된다는 것을 잊지말자!

```java

import java.util.ArrayList;
import java.util.Scanner;
public class baekjoon_1546 {
    public static void main(String[] argc){
        Scanner scanner = new Scanner(System.in);
        float iter = Integer.parseInt(scanner.next());
        float max=0;
        float all=0;
        ArrayList<Integer> arrayList = new ArrayList<>();
        for(int i=0;i<iter;i++) {
            int tmp = Integer.parseInt(scanner.next());
            if(max<=tmp) max = tmp;
            arrayList.add(tmp);
        }
        for(int i=0;i<iter;i++) {
            all+=(arrayList.get(i)/max*100);
        }
        System.out.println((float) all/iter);
    }
}


```
