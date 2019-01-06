## BaekJoon/BOJ [JAVA] 셀프 넘버_4673

HINT: 크기가 10000이기 때문에, 시간에 쫓기지 않아도 된다! 배열에 넣어서 셀프넘버가 아닌 수들을 1로 표시 해 주었다.

```java

import java.util.ArrayList;

public class baekjoon_4673 {
    public static void main(String argv[]) {
        int array[] = new int[10050];
        final int not_selfnumber = 1;
        final int selfnumber = 0;
        int i=0;
        while(i<=10000){
            int total=i;
            total+=decompose(i);
            array[total]=not_selfnumber;
            i++;
        }
        i=1;
        while(i<=10000) {
            int tmp = array[i];
            if(tmp == selfnumber) System.out.println(i+"");
            i++;
        }
    }

    public static int decompose(int num) {
        int total=0;
        while(num>=1) {
            total += (num%10);
            num/=10;
        }
        return total;
    }
}



```
