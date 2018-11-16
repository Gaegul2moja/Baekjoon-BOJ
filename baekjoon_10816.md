## BaekJoon/BOJ [JAVA] 숫자카드2_10816

HINT: Hashmap을 써보자...!!
없는 데이터를 체크 할 경우 또한 고려 해야 할 것이다...

```java

import java.util.*;
public class baekjoon_10816 {
    public static void main(String [] argc){
        Scanner scanner = new Scanner(System.in);
        int n = Integer.parseInt(scanner.next());
        HashMap<Integer, Integer> hashMap = new HashMap<>();
        ArrayList<Integer> arrayList = new ArrayList<>();
        for(int i=0;i<n;i++){
            int tmp = Integer.parseInt(scanner.next());
            if(hashMap.containsKey(tmp)) hashMap.replace(tmp, hashMap.get(tmp)+1);
            else hashMap.put(tmp, 1);
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
