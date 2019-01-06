## BaekJoon/BOJ [JAVA] 시험 성적_9498

HINT: java에서 출력 형식을 맞추는 방법은 여러가지가 있는데, 우선 DecimalFormat을 사용하는 것이고, 다른 하나는 C++처럼 printf에서 %.nf를 사용하는 것이다. 근데 DecimalFormat은 틀렸다고 나온다. 왜일까....8ㅅ8;; 그리고, 소수점 3째자리에서 반올림을 하는 방법은 Math.round를 사용해, Math.round(e*1000)/1000.0 를 이용하면 된다.

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
