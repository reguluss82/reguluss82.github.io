---
layout: default
title: "java-배열"
parent: Java study
nav_order: 15
---

# 배열 생성 및 배열의 크기
{: .no_toc }


```java
package ch04;

public class Arr01 {
		// int long...자료구조 배열도 자료구조
		// 인덱스란? 배열의 맨 처음부터의 위치이다. 
		// 주의할 점은 자바에서의 인덱스는 0부터 시작한다는 것이다
	public static void main(String[] args) {
		// 선언 후 값 지정하는 경우
		// 크기가 5인 배열 a 생성   같은 타입들
		int[] a = new int[5];
		a[0] = 7;
		a[1] = 34;
		a[2] = 67;
		a[3] = 6;
		a[4] = 234;
		
		// a.length <-- 배열 a 사이즈 측정 
		for(int i=0; i <a.length; i++) {
			System.out.println("a[" +i+"] = " + a[i]);
		}
		
		int[] b = new int[5];
		b[0] = 7;
		b[1] = 34;
		b[2] = 67;
		b[3] = 6;
		b[4] = 234;
		
		for(int i=0; i <b.length; i++) {
			//System.out.println("b[" +i+"] = " + b[i]);
			System.out.printf("b[%d] = %d" ,i, b[i]);// %d 먼저 나오는숫자 , %s 문자
			System.out.println();
		}
	}
}
```