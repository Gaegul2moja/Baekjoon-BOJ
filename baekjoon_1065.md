## BaekJoon/BOJ [JAVA] 한수_1065

HINT: 적혀있는 예시는 쓸데없다.... 흥 111->100 876->138 예시를 참고하세요

```java

import java.util.ArrayList;
import java.util.Scanner;
public class baekjoon_1065 {
    public static void main(String[] argv) {
        Scanner scanner = new Scanner(System.in);
        int input = scanner.nextInt();
        int count=0;
        for(int i=1;i<=input;i++) {
            if(figure(i)) count++;
        }
        System.out.println(count+"");
    }

    public static boolean figure(int num) {
        ArrayList<Integer>array = new ArrayList<>();
        while(num>=1) {
            array.add(num%10);
            num/=10;
        }
        int diff=0;
        boolean figure = true;
        for(int i=0;i<array.size()-1;i++) {
            if(i==0) diff = array.get(i)-array.get(i+1);
            else {
                if(diff != array.get(i)-array.get(i+1)) {figure = false;}
            }
        }
        return figure;
    }
}


```
