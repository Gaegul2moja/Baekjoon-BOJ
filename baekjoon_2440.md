## BaekJoon/BOJ [JAVA] 별찍기 - 3_2440

HINT: 별을 거꾸로 찍기 위해 조건문 안을 조금 바꾸어 주어야한다

```java
import java.util.Scanner;
public class baekjoon_2440 {
    public static void main(String[] argc){
        Scanner scanner = new Scanner(System.in);
        int num = Integer.parseInt(scanner.next());
        for(int i=num;i>=1;i--){
            int tmp=1;
            while(tmp<=i){
                System.out.print("*");
                tmp++;
            }
            System.out.println();
        }
    }
}
```
