## BaekJoon/BOJ [JAVA] 분수찾기_1193

HINT: <br/>
<img width="300" src="https://user-images.githubusercontent.com/38804451/51402432-d4be6980-1b90-11e9-988a-cd91f93b6e5f.jpg"/>
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
