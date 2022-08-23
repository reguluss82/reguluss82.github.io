---
layout: default
title: "DB-Oracle-SQL 계정생성"
parent: DB study
nav_order: 1
---

# DB Oracle 계정생성 및 권한 부여
{: .no_toc }

```SQL
-- 계정 : scott , password : tiger
CREATE USER scott IDENTIFIED BY tiger;
-- DBA 권한(관리자권한)을 scott 에게 부여
GRANT DBA to scott;

-- +버튼 눌러서 scott 접속 계정추가해줘야 한다.


--생활코딩 예제용 계정
CREATE USER egoing IDENTIFIED BY egoing;
GRANT DBA TO egoing;
-- 학습 편의성을 위해 관리자권한을 준것. 원래는 다양한 권한제한을 두어야함

-- 계정을 생성하면 스키마도 함께 생성됨. 그렇다고 계정 = 스키마는 아님
-- 계정마다 별도로 관리하는 스키마가 있다고 이해하자.
-- 스키마란 한마디로 정의하면 ‘데이터의 구조’ 또는 ‘데이터베이스의 설계’ 를 의미합니다. 
-- 데이터베이스 스키마는 논리적 보기를 나타내는 일종의 골격구조와 같은데요, 
-- 데이터베이스의 데이터에 적용되는 모든 제약 조건을 이 골격구조로 고안해 냅니다. 
-- 스키마는 데이터베이스를 구성하는 데이터 개체(entity), 속성(Attribute), 관계(Relationship) 
-- 및 데이터 조작시 데이터 값들이 갖는 제약 조건 등에 관해 전반적으로 정의 합니다.
-- 데이터베이스의 구조와 제약조건에 관한 전반적인 명세를 기술한 메타데이터의 집합
```
