# DML

Data manipulation language

+ Insert
+ Delete
+ Update
+ Select

## Insert

```sql
INSERT INTO TableName [(columnList)]
VALUES(dataValueList)
```

+ columnList is optional; if omitted, sql assumes a list of all columns in their original CREATE TABLE order
+ Any columns omitted must have been declared as NULL when table was created, unless DEFAULT was specified when creating column

首先选中zmynb数据库，展示列

![png](showcolumns.png)

1. Insert Values

    1. 利用具体值

    ![png](insert1.png)

    2. 利用默认值

    ![png](insert2.png)

## Basic SELECT Statement

```sql
SELECT A1,A2,...,An
FROM R1,R2,...,Rn
WHERE condition
```

- ALL Columns, All Rows

    ![png](selectall.png)

- Specific Columns, All Rows

    ![png](selectcol.png)

- Use of Distinct

    ![png](distinct.png)

- Calculated Fields (这个例子比较特殊，数据类型是char(4))

    ![png](calculate.png)

- Comparison Search Condition

    ![png](comparison.png)

- Compound Comparison Search Condition

    ![png](compoundcompare.png)

- Range Search Condition

    ![png](comparebetween.png)

- Pattern Matching

    ![png](pattern.png)

- NULL Search Condition

    ![png](null.png)

- Single Column Ordering

    - 默认从上到下升序
    - 如果要从上到下降序，需要用DESC

    ![png](order.png)

- Multiple Column Ordering

    - 先利用stupid降序，在此基础上，id升序

    ![png](multiorder.png)