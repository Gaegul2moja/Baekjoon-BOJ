## BaekJoon/BOJ [JAVA] 더하기 사이클_1110

HINT: 왜 while문 조건에 n!=tmp를 넣으면 안되는데 안에 넣으면 되는걸까....? 혹시 이 문제로 틀렸다고 뜨는 사람은 안에 넣어보시길

```java

import java.util.Scanner;
public class baekjoon_1110 {
    public static void main(String[] argc){
        Scanner scanner = new Scanner(System.in);
        int n = Integer.parseInt(scanner.next());
        int tmp=0, count=1;
        int num = n;
        while(true){
            tmp = ((num/10)+(num%10))%10;
            tmp+=((num%10)*10);
            num = tmp;
            if(n!=tmp)count++;
            else break;
        }
        System.out.println(count);
    }
}


```
