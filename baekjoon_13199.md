## BaekJoon/BOJ [JAVA] 치킨먹고싶다_13199

HINT: 상영이의 치킨개수를 유의하자
 순수 돈으로 산 치킨 개수 + (쿠폰 개수 + 쿠폰으로 산 치킨개수)/need...

```java
import java.util.*;
public class baekjoon_13199 {
    public static void main(String[] argc){
        Scanner scanner = new Scanner(System.in);
        Vector<Integer> result = new Vector<Integer>();
        int iter = scanner.nextInt();

        for(int i=0;i<iter;i++){
            int price = scanner.nextInt();
            int money = scanner.nextInt();
            int need = scanner.nextInt();
            int give = scanner.nextInt();
            result.add(calculate(price, money, need, give));
        }
        for(int i=0;i<result.size();i++) System.out.println(result.get(i));

    }
    public static int calculate(int price, int money, int need, int give){
        int sang, doo;
        int cou_num = (money/price)*give;
        int sang_cou;
        doo = (money/price)+ cou_num/need; 
        sang_cou = cou_num;
        sang = (money/price);
        while(sang_cou>=need){
            sang+=sang_cou/need;
            sang_cou = (sang_cou/need)*give + sang_cou%need;
        }
        return (sang - doo);
    }
}


```
