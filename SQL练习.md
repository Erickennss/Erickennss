# 练习题（请给出代码、包含代码及代码执行结果的截图）

## 1.1

编写一条 CREATE TABLE 语句，用来创建一个包含表 1-A 中所列各项的表 Addressbook （地址簿），并为 regist_no （注册编号）列设置主键约束

表1-A　表 Addressbook （地址簿）中的列

![图片](https://oss.linklearner.com/wonderful-sql/ch01/ch01.04%E4%B9%A0%E9%A2%981.png)

### 代码

    CREATE TABLE Addressbook

    (regist_no INTEGER NOT NULL,

    name VARCHAR(128) NOT NULL,

    address VARCHAR(256) NOT NULL,

    tel_no CHAR(10),

    mail_address CHAR(20),

    PRIMARY KEY(regist_no));

### 代码执行结果

<img src="file:///C:/Users/a/AppData/Roaming/marktext/images/2023-07-21-17-29-16-image.png" title="" alt="" width="738">

![](C:\Users\a\AppData\Roaming\marktext\images\2023-07-21-17-28-51-image.png)

## 1.2

假设在创建练习1.1中的 Addressbook 表时忘记添加如下一列 postal_code （邮政编码）了，请编写 SQL 把此列添加到 Addressbook 表中。

列名 ： postal_code

数据类型 ：定长字符串类型（长度为 8）

约束 ：不能为 NULL

### 代码

ALTER TABLE addressbook ADD COLUMN postal_code CHAR(8) NOT NULL;

### 代码执行结果

![](C:\Users\a\AppData\Roaming\marktext\images\2023-07-21-17-36-49-image.png)

![](C:\Users\a\AppData\Roaming\marktext\images\2023-07-21-17-37-07-image.png)

## 1.3 填空题

请补充如下 SQL 语句来删除 Addressbook 表。

```sql
(  DROP  ) table Addressbook;
```

## 1.4 判断题

是否可以编写 SQL 语句来恢复删除掉的 Addressbook 表？

可以，再次进行一次表的创建的操作

### 代码

    CREATE TABLE Addressbook

    (regist_no INTEGER NOT NULL,

    name VARCHAR(128) NOT NULL,

    address VARCHAR(256) NOT NULL,

    tel_no CHAR(10),

    mail_address CHAR(20),

    PRIMARY KEY(regist_no));
