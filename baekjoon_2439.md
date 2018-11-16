## BaekJoon/BOJ [JAVA] 별찍기 - 2_2439

HINT: 2438문제의 응용으로써, 이 풀이는 공백 부분을 직접 " "로 넣어서 풀었다

```java
import java.util.Scanner;
public class baekjoon_2439 {
    public static void main(String[] argc){
        Scanner scanner = new Scanner(System.in);
        int num = Integer.parseInt(scanner.next());
        for(int i=1;i<=num;i++){
            for(int j=0;j<num;j++){
                if(num-j-1>=i){
                    System.out.print(" ");
                }
                else System.out.print("*");
            }
            System.out.println();
        }
    }
}
```
