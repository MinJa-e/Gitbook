# DDL ( 데이터 정의어 )

### **DDL ( Data Definition Language )**

> \- '데이터베이스,테이블,컬럼,인덱스,PK' 등의 데이터를 생성/수정/삭제 하는 종류의 명령어들을 의미

### **DDL 명령어의 종류**

| **CREATE**   | '데이터베이스(=스키마) / 테이블'을 생성            |
| ------------ | ----------------------------------- |
| **ALTER**    | 데이터베이스 객체 ( ex : 컬럼, 인덱스, PK ) 를 수정 |
| **RENAME**   | 테이블의 이름을 변경                         |
| **DROP**     | '데이터베이스(=스키마) / 테이블'을 삭제            |
| **TRUNCATE** | 테이블의 데이터를 초기화                       |

### **CREATE**

> ```
> 1. CREATE DATABASE 데이터베이스명;
>
> 2. CREATE DATABASE 데이터베이스명 [ChARACTER SET 문자인코딩셋] [COLLATE 문자 정렬방식];
>  → CREATE DATABASE 데이터베이스명 CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
> --> utf8로 하는 게 일반적이였으나, 최근 이모지 사용을 위해 utf8mb4를 사용
>  
> 3. CREATE TABLE 테이블명 (
> 	컬럼명 데이터타입 조건
> )
> --> 데이터 타입 : NUMBER / VARCHAR / DATE 등
> --> 조건 :NOT NULL / UNIQUE / PRIMARY KEY / FOREIGN KEY / CHECK / DEFAULT / INDEX
>
> -- ※ DBMS마다 문법이 다를 수 있으니 주의바랍니다!
> ```
>
> \- '데이터베이스(=스키마) / 테이블'을 만들 때 사용하는 명령어

### **ALTER**

> ```
> 1-1. ALTER TABLE 테이블명 ADD COLUMN 컬럼명 varchar(32) NOT NULL;
> --> 컬럼 추가 ( ADD )
>
> 1-2. ALTER TABLE 테이블명 ADD PRIMARY KEY 컬럼명;
> --> 프라이머리 키 추가 ( ADD )
>
> 2. ALTER TABLE 테이블명 MODIFY COLUMN 컬럼명 varchar(16) NULL;
> --> 컬럼 변경 ( MODIFY )
>
> 3. ALTER TABLE 테이블명 CHANGE COLUMN 현재컬럼명 바꿀컬럼명 varchar(16) NULL;
> --> 컬럼 이름까지 변경 ( CHANGE )
>
> 4-1. ALTER TABLE 테이블명 DROP COLUMN 컬럼명;
> --> 컬럼 삭제 ( DROP )
>
> 4-2. ALTER TABLE 테이블명 DROP INDEX 인덱스명;
> --> 인덱스 삭제 ( DROP )
>
> 4-3. ALTER TABLE 테이블명 DROP PRIMARY KEY;
> --> 프라이머리 키 삭제 ( DROP )
>
> 5-1. ALTER TABLE 현재테이블명 RENAME 바꿀테이블명;
> --> 테이블 이름 변경 ( RENAME )
> ```
>
> \- '컬럼 / 제약 조건 / 인덱스' 등 테이블 내부의 데이터 정보를 수정할 때 사용하는 명령어

### **RENAME**

> ```
> 1. RENAME TABLE 현재테이블명 TO 바꿀테이블명;
> --> 테이블명 변경
>
> 2. RENAME TABLE 현재테이블명A TO 바꿀테이블명A,
> 		현재테이블명B TO 바꿀테이블명B;
> --> 테이블명 복수 변경
> ```
>
> \- 테이블명을 바꿀 때 사용하는 명령어로, ALTER와 달리 다수의 테이블명을 동시에 바꿀 수 있음

### **DROP**

> ```
> 1. DROP DATABASE 데이터베이스명;
> 2. DROP TABLE 테이블명;
> ```
>
> \- '데이터베이스(=스키마) / 테이블'을 통째로 삭제하는 명령어

### **TRUNCATE**

> ```
> 1. TRUNCATE TABLE 테이블명;
> ```
>
> \- 해당 테이블의 데이터를 초기화하는 명령어\
> ※ DROP : 테이블(데이터베이스) 자체를 삭제 <-> TRUNCATE : 테이블의 데이터를 삭제
