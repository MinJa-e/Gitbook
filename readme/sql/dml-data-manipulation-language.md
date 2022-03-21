# DML ( 데이터 조회어 )

### **DML ( Data Manipulation Language )**

> \- 데이터를 조회 및 조작하는 명령어들

### **DML 명령어의 종류**

| **SELECT** | 데이터를 조회하는 명령어      |
| ---------- | ------------------ |
| **INSERT** | 테이블에 데이터를 삽입하는 명령어 |
| **UPDATE** | 테이블의 데이터를 수정하는 명령어 |
| **DELETE** | 테이블의 데이터를 삭제하는 명령어 |

### **INSERT**

> ```
> 1. INSERT INTO 테이블명 ( [컬럼명1], [컬럼명2], ... ) VALUES ( [값1], [값2], ... )
> --> INSERT문의 괄호에 명시된 컬럼의 순서에 따라 VALUES의 값을 삽입
>
> 2. INSERT INTO 테이블명 VALUES ( [값1], [값2], ... )
> --> 테이블에 설정된 컬럼의 순서에 맞춰 VALUES의 값을 삽입
> --> 이 때, 자동 증가 컬럼은 생략하고 넘어감
>
> 3. INSERT INTO 테이블명A ( [컬럼명1], [컬럼명2], ...) SELECT [값1], [값2], ... FROM 테이블명B
> --> INSERT문의 괄호에 명시된 컬럼명에 SELECT된 값을 삽입
>
> 4. INSERT INTO 테이블명A SELECT [값1] , [값2], ... FROM 테이블명B
> --> 2번과 마찬가지로. 테이블의 컬럼 순서에 맞춰 SELECT된 값을 삽입
>
>
> -- ※ DBMS에 따라, INTO는 생략 가능
> ```
>
> \- 테이블에 데이터를 삽입하는 명령어

### **UPDATE**

> ```
> 1. UPDATE 테이블명 SET [컬럼명1]=[값1], [컬럼명2]=[값2], ... [WHERE 조건절]
> ex) UPDATE table_a SET name = 'jae', age = 28 WHERE no=1
> --> 컬렴명에 매칭된 값으로 데이터를 수정합니다.
> --> WHERE절을 쓰지 않으면 해당 컬럼 전체가 수정됩니다.
>
> 2. UPDATE 테이블명A SET [컬럼명1]=[값2] FROM 테이블명B
> ex) UPDATE table_a
>     SET count = table_a.count + table_b.count
>     FROM (select * from table_B)
>     WHERE table_a.no = table_b.no
> --> 테이블 A와 B의 no컬럼이 같은 데이터만 count를 수정
> --> 일반적으로 사용되는 형식은 아님
> ```
>
> \- 테이블의 데이터를 수정하는 명령어

### **DELETE**

> ```
> 1. DELETE [FROM] 테이블명 [WHERE 조건절];
> --> 조건에 해당하는 테이블의 데이터를 삭제
> --> WHERE 조건절이 없을 경우엔, 전체 컬럼을 삭제
> --> ( TRUNCATE와 같다고 생각할 수 있지만, 작업방식 다름 )
> ```
>
> \- 조건에 해당하는 테이블의 데이터를 삭제하는 명령어\
> \- 조건절 없이 전체 삭제 시, TRUNCATE와 결과는 같을 수 있지만 작업 방식 및 속도 등은 다름

※ SELECT문은 따로 포스팅 예정입니다 :)
