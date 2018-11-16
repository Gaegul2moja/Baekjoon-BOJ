## BaekJoon/BOJ [JAVA] 괄호_9012

HINT: stack을 써보자! '('이면, stack에 넣고, ')'이면 stack에서 pop한다.

```java

import java.util.*;
public class baekjoon_9012 {
    public static void main(String[] argc){
        Scanner scanner = new Scanner(System.in);
        int num = Integer.parseInt(scanner.nextLine());
        int check=1;
        for(int i=0;i<num;i++){
            String line = scanner.nextLine();
            Stack<Character> stack = new Stack<>();
            for(int j=0;j<line.length();j++){
                if(line.charAt(j)=='(') stack.push('(');
                else if(line.charAt(j)==')'){
                    if(!stack.isEmpty()) stack.pop();
                    else check=0;
                }
            }
            if(stack.isEmpty()&&check==1) {System.out.println("YES"); check=1;}
            else {System.out.println("NO");check=1;}
        }
    }
}


```
