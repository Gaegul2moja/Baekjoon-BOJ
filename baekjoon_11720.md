## BaekJoon/BOJ [JAVA] 숫자의 합_11720

HINT: 문자열이 공백으로 구분되어 들어오지 않기 때문에(공백없이), 우선 String으로 받고, index별로 integer로 바꾸어 합해 주었다

```java

import java.util.Scanner;
public class baekjoon_11720 {
    public static void main(String[] argc){
        Scanner scanner = new Scanner(System.in);
        int iter = Integer.parseInt(scanner.next());
        String input = scanner.next();
        int total=0;
        for(int i=0;i<iter;i++){
            total+=Integer.parseInt(input.charAt(i)+"");
        }
        scanner.close(); 
        System.out.println(total);
    }
}


```
