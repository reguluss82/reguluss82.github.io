---
layout: default
title: "Java-Continue와 break"
parent: Java study
nav_order: 14
---

# Continue 사용법
{: .no_toc }

```java
package ch03;

public class Continue1 {

	public static void main(String[] args) {
		for (int i = 0; i < 10 ; i ++) {
			System.out.println("대박 i = " + i );
			if ( i > 5) continue;  // 만나면 해당 반복부분 탈출 후 다음반복실행 /break; 만나는 즉시 반복문 전체 탈출
			System.out.println("쪽박 i = " + i);
		}

	}

}
```

# break 사용법
{: .no_toc }

```java
package ch03;

public class Break1 {

	public static void main(String[] args) {
		int num = 0, sum = 0;
		while (true) {
			num ++;
			sum+= num;
			System.out.println("sum->"+sum);
			if(num==5) break;
			// Break 반복문, 분기문 종료
		}
		System.out.println("합계" + sum);
		System.out.println("끝");
	}

}
```