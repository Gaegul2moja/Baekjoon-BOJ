## BaekJoon/BOJ [JAVA] X보다 작은 수_10871

HINT: 입력받으면서 구분해 arraylist에 넣어 주었다!

```java

import java.util.ArrayList;
import java.util.Scanner;
public class baekjoon_10871 {
    public static void main(String[] argc){
        Scanner scanner = new Scanner(System.in);
        int iter = Integer.parseInt(scanner.next());
        int num = Integer.parseInt(scanner.next());
        ArrayList<Integer> arrayList = new ArrayList<>();
        for(int i=0;i<iter;i++) {
            int tmp = Integer.parseInt(scanner.next());
            if(tmp<num) arrayList.add(tmp);
        }
        for(int i=0;i<arrayList.size();i++)
            System.out.print(arrayList.get(i)+" ");
        System.out.println();
        scanner.close();
    }
}


```
