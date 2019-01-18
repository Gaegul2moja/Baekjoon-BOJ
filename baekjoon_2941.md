## BaekJoon/BOJ [JAVA] 크로아티아 알파벳_2941

HINT: 경우의 수를 나누고 count_length는 특수한(표에 나와있는)크로아티아 알파벳의 길이를, count는 특수한 크로아티아 알파벳의 수를 세었다

```java

import java.util.Scanner;
public class baekjoon_2941 {
    public static void main(String[] argc) {
        Scanner scanner = new Scanner(System.in);
        String input = scanner.nextLine();

        int count=0; int length_count=0;
        for(int i = 0; i < input.length() - 1; i++) {
            switch(input.charAt(i)) {
                case 'c':
                    if(input.charAt(i+1)=='=') {count++; length_count+=2;}
                    else if(input.charAt(i+1)=='-') {count++; length_count+=2;}
                    break;
                case 'd':
                    if(input.charAt(i+1)=='z') {
                        if(i+2<=input.length()) {
                            if(input.charAt(i+2)=='=') {count++; length_count+=3;}
                        }
                    }
                    else if(input.charAt(i+1)=='-') {count++; length_count+=2;}
                    break;
                case 'l':
                case 'n':
                    if(input.charAt(i+1)=='j') {count++; length_count+=2;}
                    break;
                case 's':
                    if(input.charAt(i+1)=='=') {count++; length_count+=2;}
                    break;
                case 'z':
                    if(input.charAt(i+1)=='=') {
                        if(i>0) {
                            if(input.charAt(i-1)!='d') {count++; length_count+=2;}
                        }
                    }
                    break;
                default:
            }
        }
        System.out.println(input.length()-length_count+count);
    }
}


```
