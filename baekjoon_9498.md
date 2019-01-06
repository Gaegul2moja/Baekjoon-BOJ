## BaekJoon/BOJ [JAVA] 시험 성적_9498

HINT: 단순한 if문이다

```java

import java.util.Scanner;
public class baekjoon_9498 {
    public static void main(String [] argc){
        Scanner scanner = new Scanner(System.in);
        int score = Integer.parseInt(scanner.next());

        if(score>=90 && score<=100) System.out.println("A");
        else if(score>=80 && score<=89) System.out.println("B");
        else if(score>=70 && score<=79) System.out.println("C");
        else if(score>=60 && score<=69) System.out.println("D");
        else System.out.println("F");
    }
}


```
