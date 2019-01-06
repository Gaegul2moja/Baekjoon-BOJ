## BaekJoon/BOJ [JAVA] 알파벳 찾기_10809

HINT: vector에서 해당 인덱스의 요소를 수정하는 것은 add가 아니라 set이다. 뭐...절대 내가 헷갈리고 삽질해서 알려주는건 아니다.

```java

import java.util.Scanner;
import java.util.Vector;

public class baekjoon_10809 {
    public static void main(String[] argc) {
        Scanner scanner = new Scanner(System.in);
        String input_word = scanner.nextLine();
        Vector<Integer> word_check = new Vector<>();

        for(int count = 0; count<26; count++) word_check.add(-1);

        for(int word_location = 0; word_location < input_word.length(); word_location++) {
            int tmp_check_location = (int)input_word.charAt(word_location)-97;
            if(word_check.elementAt(tmp_check_location)==-1) word_check.set(tmp_check_location,word_location);
        }
        for(int vector_count = 0; vector_count < word_check.size(); vector_count++) System.out.print(word_check.elementAt(vector_count)+" ");
    }
}


```
