## BaekJoon/BOJ [JAVA] 구구단_2739

HINT: 구구단 출력시, 공백은 상관 없는듯 하다

```java

import java.util.Scanner;
public class baekjoon_2739 {
    public static void main(String[] argc){
        Scanner scanner = new Scanner(System.in);
        int num = Integer.parseInt(scanner.next());
        scanner.close();
        for(int i=1;i<10;i++){
            System.out.println(num+" * "+i+" = "+(num*i));
        }
    }
}


```
