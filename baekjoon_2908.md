## BaekJoon/BOJ [JAVA] 상수_2908

HINT: Java에서는 문자열 더하기를 할 수 있다

```java

import java.util.Scanner;
public class baekjoon_2908 {
    public static void main(String[] argc) {
        Scanner scanner = new Scanner(System.in);
        String a = scanner.next();
        String b = scanner.next();

        String a_tmp="";
        for(int i=a.length()-1;i>=0;i--) {
            a_tmp+=a.charAt(i);
        }
        String b_tmp="";
        for(int i=b.length()-1;i>=0;i--) {
            b_tmp+=b.charAt(i);
        }
        if(Integer.parseInt(a_tmp)>Integer.parseInt(b_tmp))
            System.out.println(a_tmp);
        else System.out.println(b_tmp);
    }
}


```
