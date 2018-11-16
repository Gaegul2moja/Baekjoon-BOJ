## BaekJoon/BOJ [JAVA] 2007년_1924

HINT: 달 별, 일자수를 배열로 저장 해 계산한다

```java

import java.util.Scanner;
public class baekjoon_1924 {
	public static void main(String[] args) {
		Scanner scanner = new Scanner(System.in);
		int month = scanner.nextInt();
		int date = scanner.nextInt();
		int result=0;
		int arr[] = {0,31,28,31,30,31,30,31,31,30,31,30,31};
		for(int i=1;i<month;i++){
			result+=arr[i];
		}
		result+=date;
		int day=result%7;
		if(day==1) System.out.println("MON");
		else if(day==2) System.out.println("TUE");
		else if(day==3) System.out.println("WED");
		else if(day==4) System.out.println("THU");
		else if(day==5) System.out.println("FRI");
		else if(day==6) System.out.println("SAT");
		else if(day==0) System.out.println("SUN");
	}

}

```
