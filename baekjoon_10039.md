## BaekJoon/BOJ [JAVA] 평균 점수_10039

HINT: 그냥 더하면 되는 쉬운 문제 굳이 배열 쓸 필요도 없는...?

```java

import java.util.Scanner;

public class baekjoon_10039 {
    public static void main(String[] argc) {
        Scanner scanner = new Scanner(System.in);
        int total=0;
        for(int iter_count = 0; iter_count < 5; iter_count++) {
            int tmp_input = Integer.parseInt(scanner.nextLine());
            if(tmp_input>=40) total+=tmp_input;
            else total+=40;
        }
        System.out.println(total/5);
    }
}


```
