## BaekJoon/BOJ [JAVA] 합_8393

HINT: 다 더하자

```java

import java.util.Scanner;
public class baekjoon_8393 {
    public static void main(String[] argc){
        Scanner scanner = new Scanner(System.in);
        int num = Integer.parseInt(scanner.next());
        int total=0;
        for(int i=1;i<=num;i++){
            total+=i;
        }
        System.out.println(total);
    }
}


```
