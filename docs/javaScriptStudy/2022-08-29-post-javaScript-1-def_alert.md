---
layout: default
title: "javaScript 개념과 alert메소드"
parent: javaScript study
nav_order: 1
---

# javaScript 개념과 alert메소드
{: .no_toc }

```js
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Insert title here</title>
<script type="text/javascript">
	alert("대박\n사건");
	var a = prompt("보고 싶은 구구단은 몇 단?", "7"); /* "7" <- default값 */
	alert("a->"+a);
/*
prompt 메소드
window 객체의 prompt() 메소드는 사용자에게 간단한 메시지를 보여주고,
사용자가 입력한 문자열을 반환
사용자가 대화 상자에 입력한 텍스트를 문자열 타입으로 반환

alert 메소드
자바스크립트에서 가장 간단하게 데이터를 출력할 수 있는 방법
브라우저와는 별도의 대화 상자를 띄워 사용자에게 데이터를 전달
*/  
</script>
</head>
<body>
 <h2>자바 스크립트의 개념</h2>
- 자바스크립트(JavaScript)는 객체(object) 기반의 스크립트 언어.<br>
- HTML로는 웹의 내용을 작성하고, CSS로는 웹을 디자인하며, 자바스크립트로는 웹의 동작을 구현<br>
- 자바스크립트는 주로 웹 브라우저에서 사용되나, Node.js와 같은 프레임워크를 사용하면 서버 측
프로그래밍에서도 사용<br>
- 현재 컴퓨터나 스마트폰 등에 포함된 대부분의 웹 브라우저에는 자바스크립트 인터프리터가 내장<br>

<h2>자바 스크립트의 특징</h2>
- 인터프리터 언어 (이러한 컴파일 작업을 거치지 않고, 소스 코드를 바로 실행할 수 있는 언어를 의미)<br>
- 유니코드 기반의 프로그래밍 언어 - 대소문자 구별<br>
- 서버가 아닌 클라이언트에서 번역해서 실행<br>
- 동적 바인딩이 가능 - 객체 지향형 언어.<br>
- HTML 문서에 혼합하여 사용.<br>
- 변수의 형(type)을 지정할 필요가 없음 .<br>
- 인터렉티브(interactive)한 홈페이지 구축 가능<br>
- 객체 지향형 프로그래밍과 함수형 프로그래밍을 모두 표현<br>
</body>
</html>
```