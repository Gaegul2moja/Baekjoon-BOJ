## BaekJoon/BOJ [JAVA] 숫자카드_10815

단계: Hashmap을 써서 있는지 없는지 체크하자

```java
import java.util.*;
public class baekjoon_10815 {
    public static void main(String [] argc){
        Scanner scanner = new Scanner(System.in);
        int n = Integer.parseInt(scanner.next());
        HashMap<Integer, Integer> hashMap = new HashMap<>();
        ArrayList<Integer> arrayList = new ArrayList<>();
        for(int i=0;i<n;i++){
            int tmp = Integer.parseInt(scanner.next());
            if(!hashMap.containsKey(tmp)) hashMap.put(tmp, 1);
        }
        int m = Integer.parseInt(scanner.next());
        for(int j=0;j<m;j++){
            int check = Integer.parseInt(scanner.next());
            if(hashMap.containsKey(check)) arrayList.add(hashMap.get(check));
            else arrayList.add(0);
        }
        for(int z=0;z<m;z++) System.out.print(arrayList.get(z)+" ");
        System.out.println();
    }
}

```
