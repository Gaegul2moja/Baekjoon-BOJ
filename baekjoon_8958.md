## BaekJoon/BOJ [JAVA] OX 퀴즈_8958

HINT: 다시 한번 깨달은 클린코드의 중요성....바보같지만 중첩 for문의 변수를 둘다 i를 써놨었다....

```java

import java.util.Scanner;
import java.util.Vector;

public class baekjoon_8958 {
    public static void main(String[] argc) {
        Scanner scanner = new Scanner(System.in);
        Vector<Integer> result = new Vector<>();
        int iter = Integer.parseInt(scanner.nextLine());
        for(int i = 0; i < iter; i++) {
            String input = scanner.nextLine();
            int count=0, score=0;
//            System.out.print("*"+input+"*");
            for(int j=0;j<input.length();j++) {
//                System.out.print("["+input.charAt(j)+"]");
                if(input.charAt(j)=='O') { count++; }
                else { count=0; }
//                System.out.print("count: "+count+"-i: "+j+"/");
                score+=count;
            }
            result.add(score);
//            System.out.println();
        }
        for(int i=0;i<result.size();i++) System.out.println(result.elementAt(i));

    }
}



```
