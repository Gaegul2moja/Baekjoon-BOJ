## BaekJoon/BOJ [JAVA] 열 개씩 끊어 출력하기_11721

HINT: String으로 받은 문자열의 index가 10으로 나누어 떨어지면, "\n"을 출력하는 방식 - 그러면 처음 i가 0일 경우에도 "\n"이 되므로, 고려 해 주어야한다.

```java
import java.util.Scanner;
public class baekjoon_11721 {
    public static void main(String[] argc){
        Scanner scanner = new Scanner(System.in);
        String input = scanner.nextLine();
        for(int i=0;i<input.length();i++){
            if(i%10==0&&i!=0) System.out.println();
            System.out.print(input.charAt(i));
        }
        scanner.close();
    }
}

```
