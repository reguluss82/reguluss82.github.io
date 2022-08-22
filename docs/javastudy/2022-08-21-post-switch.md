---
title: "Java-switch"
excerpt_separator: "<!--more-->"
categories:
  - Blog
tags:
  - java
---
switch 사용법과 integer.parsint에 대해
```java
package ch03;

public class Sw1 {

	public static void main(String[] args) {
		int num = Integer.parseInt(args[0]);
//Integer.parseInt(args[0]); ->첫번째 들어온 args[0] 의 값을 숫자형태로 바꾸려고 하는 메소드
//왜냐하면 args[0]  은 문자열 형태의 데이타. String [ ] args  라고 선언..이값이 실제로  "1" 이라는 값이라도 이것은 문자열입니다.
//"1"->1  이라는 숫자로 바꾸고 싶다는 뜻
//args[1] 이면 argument 두번째 값(1번째 문자열) (0이면 첫번째값 (0번째 문자열))
//args[0] 값이 없기 때문에  args[0] 0번째 문자열을  정해줘야 오류 x
//오류ex)Exception in thread "main" java.lang.ArrayIndexOutOfBoundsException: Index 0 out of bounds for length 0
//arg 입력 방법 해당 클래스 파일 우클-> run as -> run config -> arguments -> program arguments 12

		switch (num) {
		case 1:
			System.out.println("L");
			break; //break;  하지 않으면 오류가 생길수 있다
		case 2:
			System.out.println("O");
			break;
		// 두줄이든 한줄이든
		case 3:
			System.out.println("V");
			break;
		case 4:
			System.out.println("E");
			break;
		default:
			System.out.println("똑바로 해");
		}

	}

}
```
