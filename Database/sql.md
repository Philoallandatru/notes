



# SQL

#### SQL的组成部分

- **Data-definitionlanguage**(DDL)
- **Data-manipulation language** (DML)
- **Integrity**.
- **View definition**
- **Transaction control**
- **Embedded** **SQL** and **dynamic** **SQL**
- **Authorization**

#### **Basic Structure of SQL Queries

##### **Queries on a Single Relation** 单关系查询

#### 

```sql
select ID, name, dept from instructor;
name, salary * 1.1
```



##### **Queries on Multiple Relations** 多关系查询



#### 集合运算

##### 

##### Union 并

To find the set of all courses taught either in Fall 2009 or in Spring 2010, or both, we write

The **union** operation automatically eliminates duplicates,

If we want to retain all duplicates, we must write **union all** in place of **union**:

```sql
(select course
from section
where semester = ’Fall’ and year= 2009)
id from section
id
 union all (select course
 where semester = ’Spring’ and year= 2010);
```

##### **The Intersect Operation** 交

The **intersect** operation automatically eliminates duplicates. If we want to retain all duplicates, we must write **intersect all** in place of **intersect**。

##### **The Except Operation** 补

The **except** operation outputs all tuples from its first input that do not occur in the second input

##### Not 非



#### Aggregate functions 聚合函数

- Average:**avg**
- **Minimum:** min
- Maximum:**max**
- Total:**sum**
- **Count:** count

#### **Nested Subqueries**

SQL allows testing tuples for membership in a relation. The **in** connective tests for set membership, where the set is a collection of values produced by a **select** clause. The **not in** connective tests for the absence of set membership.

##### **Set Comparison**





#### 组成部分

- 

```sql
CREATE TABLE student (
    sid INT PRIMARY KEY,
    name VARCHAR(16),
    login VARCHAR(32) UNIQUE,
    age SMALLINT,
    gpa FLOAT
);

CREATE TABLE course (
    cid VARCHAR(32) PRIMARY KEY,
    name VARCHAR(32) NOT NULL
);

CREATE TABLE enrolled (
    sid INT REFERENCES student (sid),
    cid VARCHAR(32) REFERENCES course (cid),
    grade CHAR(1)
);

```



##### select

```sql
SELECT s.name
FROM enrolled AS e, student AS s
WHERE e.grade = 'A' AND e.cid = '15-721'
AND e.sid = s.sid;
```

