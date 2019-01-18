## BaekJoon/BOJ [JAVA] 단어공부_1157

HINT: 백준은 잘못이 없습니다. 제 머리탓이지요... max를 초반만 구하고 break 해 버리는 멍청한 짓을 한건 안비밀
(추가 예시: aasdjhfgjkjkjghubg -> j)

```java

import java.util.Scanner;
import java.util.Vector;

public class baekjoon_1157 {
    public static void main (String[] argc) {
        Scanner scanner = new Scanner(System.in);
        String input = scanner.nextLine().toUpperCase();
        Vector<Integer> alpha = new Vector<>();
        for(int i=0;i<26;i++) alpha.add(0);

        for(int i=0;i<input.length();i++) {
            alpha.set((int)input.charAt(i)-65,alpha.elementAt((input.charAt(i)-65))+1);
        }

        int max=0,maxcount=0;
        for(int i=0;i<26;i++) {
            int tmp_i = alpha.elementAt(i);
            if(tmp_i>max && tmp_i!=0) {max = tmp_i; maxcount=0;}
            else if(max==tmp_i && tmp_i!=0) { maxcount++; }

        }
        if(maxcount!=0||input.length()==0) System.out.println("?");
        else System.out.println((char)(alpha.indexOf(max)+65));
    }
}


```
