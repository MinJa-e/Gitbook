# SQL 언어의 종류

### **SQL ( Structured Query Language )**

> \- SQL( Structured Query Language )이란, 단어 그대로 '구조적인 질의 언어'라는 의미.\
> \- 이 SQL이란 언어를 통해 데이터베이스를 제어하고 관리함.

### **SQL 언어의 종류**

| <p><strong>DDL</strong><br><strong>( Data Definition Language )</strong><br></p>     | <p>- 데이터 베이스 객체를 정의 하거나 조작하기 위해 사용<br>- SCHEMA, DOMAIN, TABLE, VIEW, INDEX 를 정의, 변경, 삭제<br>( ex : CREATE, ALTER,  RENAME, DROP, TRUNCATE )<br></p> |
| ------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p><strong>DML</strong><br><strong>( Data Manipulation Language )</strong><br></p>   | <p>- 데이터를 조작 (조회, 삽입, 수정, 삭제) 하기 위해 사용<br>- 사용자가 응용 프로그램과 데이터 베이스 사이에 실질적인 데이터 처리를 위해서 주로 사용<br>( ex : SELECT, INSERT, DELETE, UPDATE )</p>        |
| <p><strong>DCL</strong><br><strong>( Data Control Language )</strong></p>            | <p>- 데이터를 제어하는 언어<br>- 데이터의 보안, 무결성, 회복, 병행 수행제어 등을 정의하는데 사용<br>( ex : COMMIT, ROLLBACK, SAVEPOINT, GRANT, REVOKE )</p>                            |
| <p><strong>DQL</strong><br><strong>( Data Query Language )</strong><br></p>          | - DDL에서 SELECT문만 따로 분리하여 DQL이라고도 함.                                                                                                                |
| <p><strong>TCL</strong><br><strong>( Transaction Control Language )</strong><br></p> | - DCL에서 'COMMIT, ROLLBACK, SAVEPOINT'만을 분리하여 TCL이라고도 함.                                                                                            |
