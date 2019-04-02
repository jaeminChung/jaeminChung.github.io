---
layout: post
title:  "PostgreSQL에서 다른 DB테이블과의 연결 만들기"
date:   2019-01-02 22:35:13
categories: programming
permalink: /archivers/PostgreSQL에서다른DB연결
---
1. extension 설치
```sql
CREATE EXTENSION postgres_fdw;
```
2. 서버 설정
```sql
CREATE SERVER db_other FOREIGN DATA WRAPPER postgres_fdw
OPTIONS (host '192.168.0.1', dbname 'db_other', port '5432');
```
3. 사용자 설정
```sql
CREATE USER MAPPING FOR postgres SERVER db_other
OPTIONS (user 'postgres', password '1234');
```
4. 원격 테이블 생성 (테이블명과 컬럼이 일치해야 함)
```sql
CREATE FOREIGN TABLE tb_program (
  program_name character varying(200) collate pg_catalog."default" not null,
  ...
)
SERVER db_other;
```
