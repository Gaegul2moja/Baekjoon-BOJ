## BaekJoon/BOJ [JAVA] 그룹단어 체커_1316

HINT: 배열 초기값이 0인거랑 index 0 이랑 겹쳐서 이상한짓 하고있었다.... 그래서 차피 알파벳이니까 -1로 초기화 했다.

```java

import java.util.Scanner;
public class baekjoon_1316 {
    public static void main(String[] argc) {

        Scanner scanner = new Scanner(System.in);
        int iter = Integer.parseInt(scanner.nextLine());
        int count=0;
        while(iter-->0){
            String input = scanner.nextLine();
            int alpha[] = new int[26];
            for(int i=0;i<26;i++) alpha[i] = -1;
            boolean figure = true;
            for(int i=0;i<input.length();i++) {
                int location = (int)input.charAt(i)-97;
                if(alpha[location] == -1 ) alpha[location] = i;
                else {
                    if((i-alpha[location])==1) { alpha[location] = i; }
                    else figure = false;
                }
            }
            if(figure) count++;
        }
        System.out.println(count);
    }
}



```
