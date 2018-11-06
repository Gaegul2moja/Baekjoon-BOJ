BaekJoon/BOJ [JAVA] 치킨배달_15686
========================

<p>
<h3>HINT: </h3>
장사가 안되는 지점은 가차없이 없애버리는 치킨 본사의 잔인한 영업방식을 알 수 있는 문제입니다. 다행이 지점과 집사이의 거리 즉, 두 칸 (r1, c1)과 (r2, c2) 사이의 거리는 |r1-r2| + |c1-c2|로 쉽게 구합니다.
</p>
<h3>입력 조건: </h3>
첫째 줄에 N(2 ≤ N ≤ 50)과 M(1 ≤ M ≤ 13)이 주어진다.
둘째 줄부터 N개의 줄에는 도시의 정보가 주어진다.
도시의 정보는 0, 1, 2로 이루어져 있고, 0은 빈 칸, 1은 집, 2는 치킨집을 의미한다. 집의 개수는 2N개를 넘지 않으며, 적어도 1개는 존재한다. 치킨집의 개수는 M보다 크거나 같고, 13보다 작거나 같다.
</p>
<h3>출력조건: </h3>
첫째 줄에 폐업시키지 않을 치킨집을 최대 M개를 골랐을 때, 도시의 치킨 거리의 최솟값을 출력한다.
</p>

``` java
import java.util.*;
public class baekjoon_15686 {

    static Vector<Loc> chicken,house;
    static int h_num, c_num;
    static int minimum = Integer.MAX_VALUE;

    public static void main(String[] argc){
        Scanner scanner = new Scanner(System.in);
        h_num = scanner.nextInt();
        c_num = scanner.nextInt();

        house = new Vector<Loc>();
        chicken = new Vector<Loc>();
        Vector<Loc> answer = new Vector<Loc>();

        for(int i=0;i<h_num;i++){
            for(int j=0;j<h_num;j++){
                int tmp = scanner.nextInt();
                if(tmp == 1) house.add(new Loc(i,j));
                else if(tmp ==2)chicken.add(new Loc(i,j));
            }
        } //input
        boolean check[] = new boolean[chicken.size()];
        dfs(0,0,answer, check);
        System.out.println(minimum);
    }
    public static void dfs(int start, int depth, Vector<Loc> answer, boolean[] check){
        if(depth == c_num){
            int sum = calculate(answer);
            minimum = Math.min(minimum, sum);
            return;
        }
        for(int i=start;i<chicken.size();i++){
            if(!check[i]){
                check[i]=true;
                answer.add(chicken.get(i));
                dfs(i+1,depth+1,answer,check);
                answer.remove((answer.size()-1));
                check[i] = false;
            }
        }
    }
        public static int calculate(Vector<Loc> answer){
            int sum = 0;
            for(int i=0;i<house.size();i++){
                Loc loc_1 = house.get(i);
                int len = Integer.MAX_VALUE;
                for(int j=0;j<answer.size();j++){
                    Loc loc_2 = answer.get(j);
                    int tmp = Math.abs(loc_1.x-loc_2.x) + Math.abs(loc_1.y-loc_2.y);
                    len = Math.min(len, tmp);
                }
            sum += len;
            }
            return sum;
    }
}
class Loc{
    int x, y;
    Loc(int x, int y){
        this.x = x;
        this.y = y;
    }
}
```
================================
<p>
<h3>설명: </h3>
치킨집과 집의 위치를 저장하는 vector를 생성합니다. (int x, int y로 이루어진 Loc class 를 만들어 사용) 정답이 될 minimum은 후의 계산을 위해, Integer.MAX_VALUE로 무한 값을 넣는다.
<br/><br/>
input을 받으며, 그 값이 1일 경우, house vector에 넣고, 그 값이 2일 경우, chicken vector에 넣는다.
<br/><br/>
dfs를 사용할 겁니다. dfs함수를 만들어 줍시다. 만약 depth가 c_num 이라면 즉, 경우의 수 하나가 완성 된 경우, 그 경우의 수에 대한 도시의 치킨거리를 계산하고, 그 값이 minimum인지 판단하고 return합니다. 이 과정을 재귀와 반복을 통해 모든 경우의 수를 거칩니다. 
<br/><br/>
도시의 치킨거리를 계산하는 것은 위의 HINT에 나와있습니다 :)
</p>