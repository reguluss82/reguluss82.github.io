---
layout: default
title: "Java-증감연산자"
parent: Java study
nav_order: 4
---

# 증감연산자
{: .no_toc }


```java

package ch02;

public class IncreaseDecreaseOperatorExample {
	public static void main(String[] args) {
		int x = 10;
		int y= 10;
		int z;
		
		System.out.println("-----------------------------");
		//연산자 순서대로 잘 확인하자
		x++;	//먼저 해당 연산을 수행하고 나서, 피연산자의 값을 1 증가시킴.
		++x;	//먼저 피연산자의 값을 1 증가시킨 후에 해당 연산을 진행함.
		System.out.println("1. x=" + x);
		System.out.println("--------------x=12---------------");
		y--;
		--y;
		System.out.println("2. y=" + y);
		System.out.println("----------------y=8-------------");
		z = x++;
		System.out.println("3. x=" + x);
		System.out.println("4. z=" + z);
		System.out.println("-----------------------------");		
		z = ++x;
		System.out.println("5. x=" + z);
		System.out.println("6. z=" + z);
		System.out.println("-----------------------------");	
		System.out.println("-----------------------------");
	}
}

```
