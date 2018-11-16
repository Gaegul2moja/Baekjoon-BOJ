## BaekJoon/BOJ [JAVA] 빠른 A+B_15552

HINT: BufferedReader를 사용하기에, IOException 처리가 필요하다..!! 또한, Scanner의 경우, nextInt가 존재하여, 공백에 따른 입력의 구별이 쉽지만, BufferedReader의 경우엔 다소 복잡하므로, StringTokenizer를 통해 nextToken으로 입력을 받았다. flush를 해 주지 않으면 출력이 정상적으로 진행되지 않음을 유의하자!

```java
import java.io.*;
import java.util.ArrayList;
import java.util.StringTokenizer;
import java.util.Vector;

public class baekjoon_15552 {
    public static void main(String[] argc) throws IOException{
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        BufferedWriter bw = new BufferedWriter(new OutputStreamWriter(System.out));
        int iter = Integer.parseInt(br.readLine());
        for(int i=0;i<iter;i++){
            StringTokenizer st = new StringTokenizer(br.readLine());
            int a = Integer.parseInt(st.nextToken());
            int b = Integer.parseInt(st.nextToken());
            bw.write((a+b)+"\n");
        }
        bw.flush();
        bw.close();
    }
}


```
