## BaekJoon/BOJ [JAVA] 단어의 개수_1152

HINT: ' ' 즉 공백을 기준으로 개수를 세서 계산한다면, 앞뒤의 공백을 counting하는데 문제가 생길 수 있으므로, 처음 공백이 없는 경우, 공백 후 글자가 있는 경우, 문자열의 마지막에 공백이 있을 경우로 나누어 생각해 주자

```java

import java.util.Scanner;
public class baekjoon_1152 {
    public static void main(String[] agrc){
        Scanner scanner = new Scanner(System.in);
        String input = scanner.nextLine();
        int count=0;
        for(int i=0;i<input.length();i++) {
            if(input.charAt(i)==' '&& i==input.length()-1);
            else if(input.charAt(i)==' '&&input.charAt(i+1)!=' ') {
                count++;
            }
            else if(i==0 && input.charAt(i)!=' ') count++;
        }
        System.out.println(count);
    }
}



```
