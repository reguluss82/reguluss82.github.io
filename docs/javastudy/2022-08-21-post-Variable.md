---
title: "Java-Java의 변수"
excerpt_separator: "<!--more-->"
categories:
  - Blog
tags:
  - Post Formats
  - readability
  - standard
---
<!--more-->
java의 변수사용
<!--more-->
```java
package ch02;

public class VariableExample {

	public static void main(String[] args) {
		// int라는 자료형을 가진 value라는 변수에 10을 저장 
		int value = 10;
		
		System.out.println(value);
		
		//변수 value 값을 읽고 10을 더하는 산술 연산을 수행
		//연산의 결과값을 변수 result의 초기값으로 저장
		int result = value + 10;
		
		//sout ctrl+space sysout선택 시스아웃 축약 //syso ctr+space 바로 시스아웃 나옴
		System.out.println(result);
		
	}

}
```
