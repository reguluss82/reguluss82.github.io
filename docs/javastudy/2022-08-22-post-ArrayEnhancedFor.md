---
layout: default
title: "java-배열과 향상형For문"
parent: Java study
nav_order: 16
---

# 배열과 향상형For문
{: .no_toc }


```java
package ch04;

public class Arr02 {

	public static void main(String[] args) {
		// 선언과 동시에 초기값 지정
		int[] a = new int[] {23,45,67,789,2};
		System.out.println("-------- 일반 For문 --------");
		for(int i=0; i <a.length; i++) {
			System.out.println("a[" +i+"] = " + a[i]);
		}
		// 23,45,67,789,2  <-실행후 포인터가 자동으로 다음 값으로 이동 (순서대로)
		System.out.println("-------- 향상형 For문 --------"); //실무에서 더 많이 쓰임
		for (int kk : a) {
			System.out.println("kk= " + kk);
		}

	}

}
```