---
layout: default
title: "java-ArrCopy"
parent: Java study
nav_order: 17
---

# arraycopy 배열 복사
{: .no_toc }

```java
package ch04;

public class ArrCopy {

	public static void main(String[] args) {
		int[] a = {1,2,3,4,5,6,7};			// arraycopy 같은 타입끼리만 가능하다.
		int[] b = new int [10]; 			//숫자형 배열일때 안정해주면 기본적으로 0
		System.out.println("-------------1----------------");
		System.arraycopy(a, 0, b, 0, a.length);
		pr(b);
		pr(a);
		cls(b);
		System.out.println("-------------2----------------");
		System.arraycopy(a, 0, b, 2, a.length);
		pr(b);
		cls(b);
		System.out.println("-------------3----------------");
		System.arraycopy(a, 1, b, 0, a.length-1);
		pr(b);
		cls(b);
		System.out.println("-------------4----------------");
		System.arraycopy(a, 1, b, 3, a.length-1);
		pr(b);
		cls(b);
		// System.out.println(b);  주소값출력이됨 객체이기때문
	}
	
	// 모든 원소 0으로 초기화
	public static void cls(int[] arr) {
		for (int i = 0; i < arr.length; i ++) {
			arr[i] = 0;
		}
	}
	// 모든 원소 출력
	public static void pr(int[] b) {	// a해도 괜찮음 이름이 달라도 상관없음 타입이 동일함
		for (int i = 0; i < b.length; i ++) {
			System.out.print(b[i] + "\t");
		}
	System.out.println();
	}
	
}
```