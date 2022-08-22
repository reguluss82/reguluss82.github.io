---
title: "Java-변수 scope"
excerpt_separator: "<!--more-->"
categories:
  - Blog
tags:
  - java
---

```java
package ch02;

public class VariableScopeExample {

	public static void main(String[] args) {
		int var1;
		
		if(true) {
			int var2;
			
			var1 = 10;
			var2 = 20;
			System.out.println("var1->"+var1);
			System.out.println("var2->"+var2);
		}
		//System.out.println("var2->"+var2); 그냥 치면 오류 변수 선언한 블록 범위 scope 안에서만 실행된다
	}

}
```
