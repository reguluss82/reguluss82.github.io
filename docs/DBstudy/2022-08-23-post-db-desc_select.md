---
layout: default
title: "DB-Oracle-SQL-DESC와 SELECT문"
parent: DB study
nav_order: 2
---

# DB-Oracle-SQL-DESC와 SELECT문
{: .no_toc }

```sql
DESC dept; --스키마의 내용이 나온다
--윈도우 cmd에서도 가능하다
--sqlplus scott/tiger   -sqlplus로그인
--desc dept; - dept라는 테이블의 구조를 확인(스키마의 내용)
--select * from tab; -현재 접속한 DB의 모든 테이블이름 조회

-- 주석문은 --
-- 실행 한줄한줄 / 범위 설정하면 여러줄 실행

--select 테이블에 저장된 데이터를 검색
--대소문자 구별 하지 않는다. 
--키워드는 주로 대문자. 
--테이블, 칼럼 이름은 소문자로 작성을 권장
--select 절과 from 절은 필수절
SELECT * FROM Dept;  --  *는 전체
SELECT deptno , loc FROM Dept;  --deptno , loc 열만 선택 검색

-- DEPARTMENT TBL(테이블) deptno , dname 만 검색
SELECT deptno , dname FROM DEPARTMENT;
SELECT deptno as dno , dname "부서번호" FROM DEPARTMENT;
-- 별명 부여 가능 as 별명 또는 "별명" 별명 
-- 별명에 대소문자를 구분하거나 공백 및 특수문자를 사용하는 경우 "" 사용


-- 합성 연산자
-- 학생 테이블에서 학번과 이름 칼럼을 연결하여 
-- “StudentContent”라는 별명으로 하나의 칼럼처럼 연결하여 출력 합성연산자 || 사용
SELECT studno , name FROM student;
SELECT studno , name , studno || name "StudentContent"
FROM   student; --너무 길면 키워드별로 줄 나눠서 표현 가능

-- HW1
-- 학생의 몸무게를 pound로 환산하고 칼럼 이름을 ‘weight_pound’ 라는 별명으로 출력. 
-- 1kg은 2.2pound
-- 산술연산자는 숫자 또는 날짜 타입에만 사용 가능
-- 괄호사용하여 우선순위 변경 가능
-- 별명 : Alias명 이라고 한다.
SELECT name , weight , weight*2.2 "weight_pound" 
FROM student;

-- 데이터타입 char vs varchar2 차이점. 면접질문!

-- CHAR :고정 길이의 문자열을 저장하며 최대 2,000바이트까지 저장 가능
-- 지정된 길이보다 짧은 데이터가 입력되는 경우, 나머지 공간은 공백으로 채워짐
-- 주소 데이터와 같은 편차가 심한 데이터를 입력할 때 사용하면 저장 공간이 낭비될 수 있음

-- VARCHAR2 : 가변 길이의 문자열을 저장하기 위해 사용하는 데이터 타입, 최대 4,000 바이트 저장 가능
-- 지정된 길이보다 짧은 문자열이 입력되면 뒷부분은 NULL로 처리되어 저장공간을 낭비하지 않음
-- 입력될 데이터의 편차가 심하거나 NULL 이 많이 입력되는 경우에 사용하는 것이 효율적
-- 실무에서는 CHAR 데이터 타입보다 VARCHAR2 를 많이 사용
```
