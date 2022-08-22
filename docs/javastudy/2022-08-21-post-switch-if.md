---
layout: default
title: "java-switch-if 중첩으로 사용"
parent: Java study
nav_order: 8
---

# 중첩 switch문과 if문 같이 쓰기
{: .no_toc }

```java
package ch03;

public class Sw5 {

	public static void main(String[] args) {
		int num = Integer.parseInt(args[0]);
		String season = "";
		//중첩 switch	//If else 와 비교 switch default
		switch (num) {										// 블록 구분 및 break; case 끝날때마다 쓰기
			case 12:	case 1:		case 2:
				switch (num) {
				case 12: System.out.println("초겨울"); break;
				case 1:  System.out.println("젤추워"); break;
				case 2:  System.out.println("추워");  break;
				}
				season = "겨울"; break;
			case 3:		case 4:		case 5:
				if (num == 3  || num == 4) System.out.println(" 대박"); // || or    && and
				else System.out.println("쪽");							//연산자 &&는 ||보다 우선순위가 높다
				season = "봄"; break;
			case 6:		case 7:		case 8:	 season = "여름"; break;
			case 9:		case 10:	case 11: season = "가을"; break;
			default : season = "뭐야"; break;
		}
		System.out.println(num+" 월은 "+ season+"입니다");
	}

}
```
