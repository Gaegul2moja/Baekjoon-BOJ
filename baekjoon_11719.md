BaekJoon/BOJ [JAVA] 그대로 출력하기_11719
========================

<br/>단계: 입출력 받아보기

<p>
HINT: <br/>
그대로 출력하기 11718과 같이 엔터와 공백에 영향을 받지 않고 출력하기 위해선 어떻게 해야할지 생각 해 봅시다 : )
</p>

```java
import java.util.Scanner;
public class baekjoon_11719 {
    public static void main(String[] argc){
        Scanner scanner = new Scanner(System.in);
        while(scanner.hasNextLine()) {
            String input = scanner.nextLine();
            System.out.println(input);
        }
        scanner.close();
    }
}
```
