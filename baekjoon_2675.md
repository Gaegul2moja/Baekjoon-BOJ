## BaekJoon/BOJ [JAVA] 문자열 반복_2675

HINT: 어정쩡하게 nextLine썼다가 헷갈린 케이스

```java

import java.util.Scanner;
import java.util.Vector;

public class baekjoon_2675 {
    public static void main(String[] argc) {
        Scanner scanner = new Scanner(System.in);
        int iter = Integer.parseInt(scanner.nextLine());
        Vector<String> output = new Vector<>();
        for(int i=0;i<iter;i++) {
            int count = scanner.nextInt();
            String word = scanner.next();
            String result = "";
            for(int j=0;j<word.length();j++) {
                for(int z=0;z<count;z++)
                    result+=word.charAt(j);
            }
            output.add(result);
        }
        for(int i=0;i<iter;i++) System.out.println(output.get(i));
    }
}



```
