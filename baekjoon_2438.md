## BaekJoon/BOJ [JAVA] 별찍기 - 1_2438

HINT: 반복문을 중첩하자

```java

import java.util.Scanner;
public class baekjoon_2438 {
    public static void main(String[] argc){
        Scanner scanner = new Scanner(System.in);
        int num = Integer.parseInt(scanner.next());
        for(int i=1;i<=num;i++){
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
