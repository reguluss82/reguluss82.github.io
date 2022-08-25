---
layout: default
title: "HTML 문서 기본구조"
parent: HTML study
nav_order: 1
---

# HTML 문서 기본구조
{: .no_toc }
그리고 <hn> 태그와 <img> 태그
```html
<!DOCTYPE html> <!-- 문서 유형을 지정하는 선언문 -->
<html> <!-- <html>: 웹 문서의 시작을 알림 -->
<head> <!-- <head>: 브라우저에게 웹 문서의 정보를 준다
            <head>의 내용은 웹페이지에 출력x -->
<meta charset="UTF-8">    <!-- <meta>: 문자 세트를 비롯한 문서정보 -->
<title>Basic HTML</title> <!-- 웹브라우저 탭 제목 -->
</head>
<body> <!-- <body> 실제 브라우저에 표시될 내용 -->
	<h1>시간이란1..</h1> <!-- <hn> 제목표시 태그 -->
	<h2>시간이란2..</h2>
	<h3>시간이란3..</h3>
	<h4>시간이란4..</h4>
	<h5>시간이란5..</h5>
	<p>내일 죽을 것처럼 오늘을 살고 영원히 살 것처럼 내일을 꿈꾸어라
	</p>
	<!-- <p></p> 입력한 내용 앞뒤로 빈 줄이 생기면서 텍스트 단락이 만들어짐 -->
	<img alt="시계이미지1" src="images/watch.jpg"><br>
	<img alt="책 표지" src="images/petit.jpg">
	<img alt="시계이미지2" src="images/watch2.jpg"><br>
	<!-- alt 이미지 설명 대체 텍스트 이미지 못찾았을때 나오는 부분 -->
</body>
</html>
<!-- hn br hr p strong b em i mark span div ul li ol table 
tr th td colspan rowspan caption thead tbody tfoot colgroup
a  -->
```
