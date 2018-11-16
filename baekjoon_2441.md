## BaekJoon/BOJ [JAVA] 별찍기 - 4_2441

HINT: 별을 거꾸로 찍기 위해 조건문 안을 조금 바꾸어 주어야한다.

```java
import java.util.Scanner;
public class baekjoon_2441 {
    public static void main(String[] argc){
        Scanner scanner = new Scanner(System.in);
        int num = Integer.parseInt(scanner.next());
        for(int i=num;i>=1;i--){
            for(int j=0;j<num;j++){
                if(num-j-1>=i){
                    System.out.print(" ");
                }
                else System.out.print("*");
            }
            System.out.println();
        }
    }
}
```
