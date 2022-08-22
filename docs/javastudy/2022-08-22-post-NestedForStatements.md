---
layout: default
title: "Java-중첩 for문"
parent: Java study
nav_order: 13
---

# 중첩 For문을 이용한 구구단 조회
{: .no_toc }


```java
package ch03;

public class For03 {

	public static void main(String[] args) {
		System.out.println("구구단");
		// 이중 for문 이용한 구구단 조회
		for (int i = 1; i <= 9; i++) {
			for (int j = 2; j <= 9; j++) {
				System.out.print(j+" * "+i+" = "+j*i+"\t");
			} 
			System.out.println();
		}
	}

}
```