---
layout: default
title: "Java-Do문 응용"
parent: Java study
nav_order: 11
---

# Do문 응용 if및 Scanner, Math.random() 사용
{: .no_toc }


```java
package ch03;

import java.util.Scanner;

public class Do5 {

	public static void main(String[] args) {
		// 1.객체선언
		Scanner sc = new Scanner(System.in);

		int cnt = 0, num; // Math.random() 0.0<=값<1.0 이므로 +1을 해주어야 100까지 만들 수 있다.
		int answer = (int) (Math.random() * 100) + 1; // 1~100정수,
		do {
			System.out.println("1~100 중 어떤 숫자일까요? ");
			// num = sc.nextInt();
			// 2. 관련 method(함수) 사용
			num = sc.nextInt();
			if (answer == num) {
				System.out.println(cnt + "번에 맞췄습니다 축하!!");
				break;//무한루프 방지
			} else if (answer > num) {
				System.out.println("더 큰수를 입력하세요");
			} else
				System.out.println("작은수를 입력하세요");
			cnt++;
		} while (true);
		sc.close();//sc 계속 열려있어서 닫아줘야 자원 낭비 x 최적화

	}

}
```