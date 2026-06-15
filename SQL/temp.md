# working with SQL with MySQL

when we want to store the application users data , we will use a

component called "database"

when we want to store the data in the database, based on how we

## store the data, the databases are classified into two types

## 1. relational database

when we store the data in the database in the form of table, then the

database is called as "relational database"

in relational database, the data will be stored in the form of table ,

where the table will have the data in the form of "rows and columns"

where rows are also called as "records or tuples "

where the columns are also called as "fields or attributes" '

when we want to work with "relational database" , we are going to

use a langauge called "SQL(sequel)"

when we want to perform any operation on the "relational database" ,

then we are going to use "SQL"

when we want to execute the "SQL query", we are going to use a

software called "DBMS"

any DBMS we are using for "relational database", then the DBMS is

called as "relational DBMS (RDBMS)"

the popular RDBMS are:

1. MySQL

2. Oracle

3. postgres SQL,.....................

any SQL query we need to execute, we will always "use DBMS",

in the DBMS will use a concept called "query Processor" and which is

responsible for "executing the SQL query" , query processor internally

uses a translator called "interpreter"

## in SQL, we will have the following sub-languages

## 1. Data Definition Language (DDL)

## in this we will have the following commands

## 1. create

## using this create command , we will do the following

create the "database | table | index | view | function | stored procedure

|.................."

## 2. rename

using this command "we can able to rename any table in the MySQL or

any database object , we need to change the name , we will use

rename

## 3. alter

when we create the table in MySQL, when we want to do the following

## , we will use the alter command

1. add the new column in the existing table

2. remove the column in the existing table

3. rename the any column in the existing table

4. change the any data type of the column in the existing table

5. when we want to change name of the existing table

## 4. truncate

when we want to "remove the all rows of the table, in MySQL, we will

use truncate command"

truncate command will never remove the "table structure", but remove

all rows of the table

## 5. drop

drop command is used in SQL, to "remove the database or view or

table or index or function or stored procedure"

## 2. Data Manipulation language (DML)

when we want to perform the operations on the table, we will use the

following commands in SQL:

1. Insert (using this command we can able to insert rows into the

table)

2. update (using this command we can able to update the row in the

table)

3. delete (using this command we can able to delete the row in the

table)

## 3. Data Query Language (DQL)

when want to retrieve the data from the table, in sql, we will use a

command called "select"

## 4. Data control Language (DCL)

when we want to give the access permissions to the users of the

## database, in SQL, we will use the following DCL commands

1. grant (used to give the permissions to the users READ or Write)

2. revoke(used to take back the given permissions from the users of

the database)

## 5. Transaction Control language (TCL)

all database operations can be done as "Transaction"

when we want to work with transactions, in SQL, we will use the

## following TCL commands

1. save point

save point used like a block, where the all operations are not effected

directly onto the table, when we perform any operation on the

database tables, those operation will effect only when we save

the operation

2. commit

commit is used to "save the operation permanently on the table"

3. rollback

rollback is used to perform "undo" operation

when we want to create the database in MySQL, we will use

following syntax:

```sql
create database database_name;
```

example:

```sql
create database employee_fp2_3_2026;

create database hr_2026;

create database student_2026;
```

when we want to show the all available databases in the MySQL, we

will use the following syntax:

```sql
show databases;
```

when we want to create any table, when we want work with any table

inside the database, then we will always "set the database as current

database", to set the database "current database", then we will use

the following syntax MySQL:

```sql
use database_name;
```

when we want to know the "what is current database", in the MySQL ,

## we will use the following syntax

```sql
select database() ;
```

when we want to create the table in the MySQL database, we will use

the following syntax:

```sql
create table table_name(col_name datatype constraint,

col_name datatype constraint, col_name data_type constraint,

.
.
.
coln datatype constraint)
```

here data type refers "What type of data, the column can have or can

store, we need to specify while creating the table" , while inserting

data, MySQL query processor will check given data as per the "given

data type of column" or not

## MySQL Datatypes

## 1. numeric data

for integer data:

tinyint

smallint

int

bigint

for float data:

float

double

## when we want to store the fixed decimal part or fractional part

decimal

numeric

## 2. text data

char

varchar

text

3. for year type data: year

4. for date type data: date

5. for time type data: time

6. for datetime data : datetime

when we want to only value among the multiple values, MySQL uses

a data type called "Enum"

when we want to store the multiple values as data inside the column,

then we define the column with the data type called "set"

## MySQL constraints

## in MySQL, we will have two types of constraints

## 1. integrity constraints (which are defined with in the table)

1. not null

2. unique

3. primary key

4. check

5. default

6. auto_increment

2. referential constraint(this constraint can be defined with two or

## more tables)

1. foreign key (this is used for data integrity)

## 1. not null

when we give the column with "not null" constraint, then the column

will take always "non-null data" or "column never take null values"

we can give the "not null" as a constraint to any number of columns

in MySQL table

when we give the "not null" as constraint , then the column will allow

the "duplicate" values

## 2. unique

when we give the column with "unique" constraint, then the column

will take always "distinct data" or "column never take duplicate values"

we can give the "unique" as a constraint to any number of columns

in MySQL table

when we give the "unique" as constraint , then the column will allow

the "null" values

when we want to make the column "never allow the duplicate values

and null values", then the column must define with both constraints

(not null and unique)

when we create the table column without constraint, the column will

allow the "null" values by default

in MySQL table, for any number of columns, we can able to take

both "not null and unique" as a constraints

## 3. primary key

when we define the "any column with primary key", the column will

always never allow the "null values and duplicate values"

primary key often called as "not null + unique"

in a table, only one column can be defined with "primary key"

when we want to make any column act as "primary key" column,

then the define the "column with both not null and unique"

## 4. default

when we are defining the column of the table with default constraint,

using default constraint, we can give the default value, when we are

inserting the into the column, if we are not specify the any value to

column, if the column default value, then the default value will inserted

as data of the column

the default value of the column in MySQL table is "null"

## 5. check

when we are inserting the data into a column, if we want to insert

right data into the column or if we want to validate the data what we

are inserting to the column, in MySQL we will use constraint called

"check"

while using "Check" constraint, we will give a condition, with this

condition, we can able to validate the data what we are inserting

into the column

in MySQL table, for any number of column can have "check" as

constraint

## 6. auto_increment

when we want to make the column gets data automatically by itself,

in MySQL, we will use a constraint called "auto_increment"

when we give or define auto_increment to any column, the column

must define with "either primary key or unique key"

when we give the any column with auto_increment, the column starts

getting value from "1" on wards by default , we can also can give

any start value for auto_increment column using "alter" command

the every new value in the auto_increment column , always "+1" to

the previous value of the column

## 7. foreign key

when we want to work with "foreign key", we require minimum two

tables or more

using this constraint we can able to "gets data integrity"

when we create the a table called "A" , based on the table "A", we want

to insert data in the another table called "B", here we are using a

constraint called "foreign key"

when we define a column in table called "A" with "primary key or

unique key", using this column we are validating the data in another

table called "B" , then the primary key column of the table "A", we

will uses a foreign key inside the table called "B" ,

complete insert, update and delete always verified first in the table "A"

, based on that table "b" will perform action

creating the table with name "employee" inside the database called

## "Employee_fp23_2026"

## employee

```sql
create table employee(
id int primary key auto_increment,
firstname varchar(100) not null,
lastname varchar(100) not null ,
email varchar(100) not null unique,
mobileno bigint not null unique,
location varchar(100) not null ,
zipcode int not null ,
deptid int not null,
deptname varchar(100) not null,
designation varchar(100) not null,
gender varchar(100) not null,
dob date not null,
jod date not null,
salary float not null);
```

once we create the table, we get the table structure, to see the table

structure, we will use the following syntax:

```sql
desc table_name;
```

or

```sql
describe table_name;
```

## example

```sql
describe employee;

or

desc employee;
```

## once we create the table, we will do the following operations

## insert the data into table

when we want to insert the data into table, we will use the following

syntax:

```sql
insert into table_name(col1,col2,col3..........coln)

values(val1,val2,val3,val4,.........valn)
```

or

```sql
insert into table_name

values(val1,val2,val3,........valn)
```

## example

```sql
insert into employee(firstname,lastname,email,
mobileno,location,zipcode,deptid,deptname,designation,
gender,dob,jod,salary)
values('ram','a','ram@gmail.com',9874561230,
'hyderabad',500047,101,'development',
'developer','male','1988-5-5','2009-8-8',
10000);
```

when we want to insert "multiple rows into MySQL table", we will use

## following example

code:

```sql
insert into employee(firstname,lastname,email,
mobileno,location,zipcode,deptid,deptname,designation,
gender,dob,jod,salary)
values('raj','p','raj@gmail.com',8874561230,
'chennai',400047,101,'development',
'developer','male','1989-12-5','2009-8-8',
20000),('madan','B','madan@gmail.com',7874561230,
'bangalore',478947,102,'QA',
'test engineer','male','1995-1-5','2019-8-8',
30000),
('suraj','k','suraj@gmail.com',6674561230,
'chennai',400047,101,'development',
'developer','male','1992-12-5','2013-8-8',
40000);
;
```

## retrieve the data from the table

when we want to retrieve the data from "MySQL" table, in MySQL

we will use a command called "select"

syntax:

```sql
select * from table_name; <=== get the all rows from the table
```

or

```sql
select col1, col2,col3,col4,...coln from table_name <=== to get the

specific column details from the MySQL
```

## example

```sql
select * from employee;
select id,firstname,lastname from employee;
```

## update data in the table

when we want to update the data inside the table, in MySQL we will

use a command called "update"

while updating the data using "update" command, we will always

give "Condition" , if we not give any condition while updating with

update command inside the table, then all rows are update, to avoid

this we will always use "update with condition"

syntax :

```sql
update table_name set col1=value, col2=value, col3=value,..........

coln=valn where condition;
```

## example

```sql
select salary from employee;
update employee set salary=salary+10000;
select id,salary from employee;
update employee set salary=salary+10000
where id=1004;
```

## delete the from the table

when we want to delete the data inside the table, in MySQL we will

use a command called "delete"

while deleting the data using "delete" command, we will always

give "Condition" , if we not give any condition while deleting with

delete command inside the table, then all rows are delete and it like

truncate the table, to avoid this we will always use "delete with

condition"

syntax :

```sql
delete from table_name where condition;
```

or

```sql
delete from table_name; <== it will remove all rows from the table

and it is as same as truncate
```

## example

```sql
select * from employee where id=1004;
delete from employee where id=1004;
```

## aliasing with MySQL

when we are retrieving the data from the "MySQL table" , we can

change the name of column, in the user defined format using "aliasing"

to alias the column name in the result, we will use a keyword called

"as"

syntax:

```sql
select col1 as "alias_name", col2 as "alias_name",..........

coln as "alias_name" from table name where condition
```

## example

```sql
select id as employee_id from employee;
select id as "employee id" from employee;
```

## clauses in MySQL

1. from

using this, we can specify, where are retrieving the data from the

"table or view"

2. where

using this, we can specify the condition in the select or update or

delete query

using this "We can filter the data" , based on the given condition

## example

```sql
select id, firstname,deptname from employee
where deptname='hr';

select id, firstname,deptname,location from employee
where location='chennai';
```

## 3. order by

using this clause , we can able to sort the any column data in the

result of select either in "Ascending or Descending"

when we want to sort the any column data using order by , it default

sort the given column always in Ascending order

when we want to sort the any column either in "Ascending or

descending order" , we will use the following keywords with order

by:

asc ===> ascending order

desc ===> descending order

## example

```sql
select id, firstname,deptname from employee
where deptname='hr'
order by id;
select id, firstname,deptname from employee
where deptname='hr'
order by id desc;
select id, firstname,deptname from employee
where deptname='hr'
order by 2 desc;
select * from employee order by 3 desc;
```

## 4. distinct

using this column, we can able to retrieve the "unique data from the

table"

when we are using "distinct" with one column, it always give the

unique values

when we are using "distinct" with multiple columns, it always give

the "unique rows"

syntax:

```sql
select distinct col1, col2, col3,....coln from the table_name

where cond order by column asc|desc;
```

## example

```sql
select distinct deptname from
employee;
select distinct deptname, deptid from employee;
select distinct * from employee;

select distinct deptid,deptname
from employee
order by 1 desc;
```

## 5. limit

limit clause is used to "specify how many rows only need to show in the

result"

syntax:

```sql
limit rownumber, offset;
```

offset is used to "tell how many rows need to show in the result"

row number is used to "Tell , in the result from which row number

onwards we need to display the result"

in MySQL , row number always starts from "0" onwards

while using "limit", if we give only one number, then limit is consider

as "offset" only

syntax:

```sql
select distinct col1, col2, col3,....coln from the table_name

where cond order by column asc|desc limit rownumber, offset;
```

## example

```sql
select id,firstname from employee limit 5;
select id,firstname from employee limit 2,3;
-- first highst salary
select salary from employee order by salary
desc limit 1;
-- second highst salary
select distinct salary from employee order by salary
desc limit 1,1;
-- thrid lowest salary
select distinct salary from employee order by salary
asc limit 2,1;
```

## Aggregate functions

1. max() :

using this function, we can able to find the maximum value in the

given column

2. min()

using this function, we can able to find the minimum value in the

given column

3. count()

using this function, we can able to find the "number of values" in

the given column

4. sum()

using this function , we can able to find the "sum of the all values of

given column"

5. avg()

using this function, we can able to find "average value of the given

column"

## example

```sql
select avg(salary) as "average salary"
from employee;
select min(salary) as "minimum salary"
from employee;
select max(salary) as "maximum salary"
from employee;
select sum(salary) as "sum" from
employee;
```

## 6. group by

this clause is used to "group the data based on the given column"

generally we will use the group by columns are "categorical columns"

"categorical columns" means "which able to categorize the data"

when we are working with group by, we will use the aggregate

functions

example:

gender , deptname, deptid, designation, order_date, joining date, .......

## example

```sql
-- get the employee count based on the department
select deptname, count(deptname)
as employee_count
from employee
group by deptname;

select deptname, count(deptname)
as employee_count
from employee
group by deptname order by 2 desc;

/*get the employee maximum salary
based on the department*/
select deptname, max(salary)
as employee_maximum_salary
from employee
group by deptname;
/*get the employee maximum salary
based on the department*/
select deptname, max(salary)
as employee_maximum_salary
from employee
group by deptname order by 2 desc;
```

## 7. having

having is used with "group by clause"

when we want to filter the "group by" result, along with group by

column , we will specify the condition for group by result, we will

use "having" clause

## example

-- get the employee count based on the department

```sql
select deptname, count(deptname)
as employee_count
from employee
group by deptname
having employee_count>=20;

select deptname, count(deptname)
as employee_count
from employee
group by deptname
having employee_count<=20;

select deptname, count(deptname)
as employee_count
from employee
group by deptname
having employee_count<=20

order by 2 desc;
```

## example

```sql
select location,deptname,count(deptname)
from employee
group by 1,2;
select location,deptname,count(deptname)
from employee
group by 1,2
order by 1;
```

## example

```sql
select deptname, count(deptname)
from employee
where salary>=100000
group by deptname
having count(deptname)>=10
order by 1;
```

## example

```sql
select distinct deptname, count(deptname)
from employee
where salary>=100000
group by deptname
having count(deptname)>=10
order by 1;
```

## union

union is used to "combine the multiple query results into single result"

when we use union with multiple queries, union will give the always

"unique rows"

while joining multiple query results into single result in MySQL, we

will use "union"

while joining multiple query results into single result without duplicate

rows in MySQL, we will use "union"

while joining multiple query results into single result with duplicate

rows in MySQL, we will use "union all"

while we are doing "union or union all", the column count in all

queries what we taken for union or union all operation, should be

same

when we apply the union on the queries, the union result always

come with first query column names only

## example

```sql
select id,firstname,lastname
from employee
union
select deptid,deptname,location
from employee;
```

## example

```sql
select id,firstname,lastname
from employee
union
select id,firstname,lastname
from employee;
```

## example

```sql
select id,firstname,lastname
from employee
union all
select id,firstname,lastname
from employee;
```

## MySQL operators

arithmetic operators: +, *, -, /,%

logical operators: or, and , not

bitwise operators: |, &,^

is operator:

is operator is used in MySQL, to retrieve the "any null data from the

table"

example:

salary is null <=== get the salary data from the table, where the

data is null

salary is not null <=== get the salary data from the table, where the

data is not null

in operator:

in MySQL, we will use "in" operator , to get the data from the table,

related to multiple values

in ===> related to multiple values

not in ===> not related to given multiple values

example:

location in ('hyd','che','blr')

location not in ('hyd','che','blr')

## between operator

between is used to get the data from the table for given range

col_name between cond1 and cond2;

example:

salary between 10000 and 20000;

(salary>=10000 and salary<=20000)

salary not between 10000 and 20000)

(salary<=10000 and salary>=20000)

## example

```sql
use employee_fp1_2024;

select * from employee where
salary>=10000 order by salary asc;

select * from employee where
salary<=10000 order by salary asc;

select * from employee where
salary=10000 order by salary asc;

select * from employee where
salary!=10000 order by salary asc;

select * from employee where
salary<>10000 order by salary asc;

select * from employee
where
salary between 60000 and 100000;

select * from employee
where
salary >=60000 and salary<=100000;

select * from employee
where
salary <=60000 or salary>=100000;

select * from employee
where location in ('pune','hyderabad')
order by 8;

select * from employee
where location='pune' or
location='hyderabad'
order by 8;

select * from employee
where location not in ('pune','hyderabad')
order by 8;

select * from employee
where salary is null;

select * from employee
where salary is not null;
```

## like operator

using this operator, we can able to get the data from the table

based on the given "pattern"

to create the pattern for " like" , we will use the following characters:

1. _ (this refers exactly one character)

2. % (this refers zero or more characters)

the above characters are called as "wild-card characters"

like pattern

example:

like "a%" ====> a,anil, arun, ajay, anaconda, aaaaaaaaaaaa,.....

like "%a" ===> a, ana, aba, accccccca,...................

like '%a%' ===> a,mallayya, yellamma, yadhamma,

like '_a' ===> la, ba, pa,.............

like 'a_a' ===> aba, aca, ada,..........

like '____' ===> abcd, dcbb,acbb,..........

## example

```sql
select firstname from
employee where firstname like 'a%';

select firstname from
employee where firstname like '%a';

select firstname from
employee where firstname like '%a%';

select firstname from
employee where firstname like 'a____';

select email from employee
where email like '%@%';

select salary from employee
where salary like '%45%';

select firstname from
employee where firstname like 'a%';

select firstname from
employee where firstname like '%a';

select firstname from
employee where firstname like '%a%';

select firstname from
employee where firstname like 'a____';

select email from employee
where email like '%@%';

select dob from employee
where dob like '%1998%';
```

working with duplicate tables or copy the data from one table to

another table:

in MySQL, when we want to create the duplicate table or copy the data

from one table to another table, we will have the following ways:

1. using like operator

when we create the duplicate table using like command , only the table

structure copied , but not data

when we want to create the duplicate table in MySQL, we will use the

following syntax:

```sql
create table table_name like original table_name;
```

in order to copy the data into duplicate table, while we create the duplicate table using "like" operator, we will use the following syntax
in MySQL:

```sql
insert into duplicate_table_name like select * from original_table_name;
```

## example

```sql
create table emp_fp2_3 like employee;
desc emp_fp2_3;
insert into emp_fp2_3 select * from employee;
select * from emp_fp2_3;
```

## 2. using select command

when we create the duplicate table using "Select" command , it will

copy the both "table structure and table data" into duplicate table

when we want to create the duplicate table, using select command we

will use the following syntax:

```sql
create table table_name select * from original_table_name
```

example:

```sql
create table emp_fp2_3_2
select * from employee;
desc emp_fp2_3_2;
select * from emp_fp2_3_2;
```

when we want to copy the data from one table to another table, in
MySQL we will use "select" command , when we are using the "Select"
command to copy the data, in the select command , we will give always
columns order as per the "duplicate table column order"

syntax:

```sql
insert into duplicate_table_name select col1, col2,col3, col4,.....coln
from original_table_name;
```

if the columns in the "original table" and "duplicate table" are same

in both types of the columns ,column order, column count, then we will use

the following syntax:

```sql
insert into duplciate_table_name select * from original_table_name;
```

## example

```sql
create table
dummy(firstname varchar(100) not null,
lastname varchar(100) not null,
id int primary key);
desc dummy;
insert into dummy select firstname,
lastname,id from employee;
select * from dummy;
```

## temporary tables or session tables in the MySQL

temporary table or session tables are exist in the MySQL, until we close

the MySQL workbench or MySQL command line

these table are "Memory efficient" table, these tables are automatically

deleted, when we close the MySQL workbench or command line

these tables will not be visible, when you run the following syntax:

```sql
show tables;
```

temporary tables or session tables are created in MySQL, using following

syntax:

```sql
create temporary table table_name(col1 type constraint,..........):
```

## example

```sql
create temporary table dummy3(firstname varchar(100));
desc dummy3;
insert into dummy3 values ('a');
select * from dummy3;
```

## working with "alter" command

when the table is already created inside the database, in that table if we

want to do the following actions :

1. if we want to add the new columns into existing table, in MySQL we
will use a command called "alter"
syntax:

```sql
alter table table_name add column_name data type constraint, add

column_name data type constraint, add column_name data type

constraint,..................................................
```

when we are adding the new columns into existing table using "Alter",
"alter" always add the new columns into table at end of the table by
default.

if we want to add the column into table using alter, then we specify the

position using following flags:

1. first (add the column as starting column of the table)

2. after (add the column after the given column in the alter)

## example

```sql
create table s23(firstname varchar(100),
lastname varchar(100));

desc s23;

alter table s23
add email varchar(100) not null unique,
add location varchar(100) not null;

alter table s23 add id int primary key first,
add midname varchar(100) not null;

alter table s23 add deptname
varchar(100) not null after lastname;
```

2. if we want to change the name of the columns in existing table, in

## MySQL we will use a command called "alter"

syntax:

```sql
alter table table_name change column original column_name new_column_name data type constraint, change column original column_name new_column_name data type constraint,...............
```

## example

```sql
desc s23;
alter table s23 change column id empid int;
alter table s23 add deptid int
not null after deptname,
change column
email emp_email varchar(500);
```

3. if we want to change the datatype of the columns in existing table, in
MySQL we will use a command called "alter"
syntax:

```sql
alter table table_name modify column_name data type constraint,
modify column_name datatype constraint,.......................
```

## example

```sql
desc s23;
alter table s23 add zipcode int,
modify emp_email varchar(100) not null;
alter table s23 modify zipcode bigint not null;
```

4. if we want to remove of the columns of existing table, in
MySQL we will use a command called "alter"

## syntax

```sql
alter table table_name drop column_name, drop column_name, drop
column_name,.......................
```

## example

```sql
desc s23;
alter table s23 drop emp_email, drop deptid;
```

5)if we want to change the name of the existing table, in
MySQL we will use a command called "alter"

## syntax

```sql
alter table table_name rename to new_table_name
```

## example

```sql
alter table s23 rename to s24;
desc s24;
```

6. when we want to reset the auto_increment column of the table in

MySQL, we will use "alter" command

syntax:

```sql
alter table table_name auto_increment=value;
```

## example

```sql
create table s25(id int primary key auto_increment);
insert into s25 values();
select * from s25;
alter table s25 auto_increment=10000;
```

## working with null data in MySQL

null data means "not number" or "not a string"
null refers "no value"
when we are not entered any data into column, while insertion, then MySQL can fill default as "null"
to avoid the null values inside the column of the MySQL table, we can
give the constraint called "not null"

example: Null+10000 ===>Null

```sql
create table t11(id int,firstname
varchar(100) not null, salary float);
desc t11;

insert into t11(firstname) values('a');
insert into t11(firstname) values('b');
insert into t11(firstname) values('c');
select * from t11;

insert into t11 values(100,'d',20000);
insert into t11 values(101,'e',30000);
insert into t11 values(102,'f',40000);
select * from t11;

select * from t11;
select count(*) from t11;
select count(id) from t11;
select sum(salary) from t11;
select max(salary) from t11;
select min(salary) from t11;

select * from t11
order by salary;

select * from t11
order by salary desc;

select salary,count(salary)
from t11
group by salary;

select salary,count(salary)
from t11
group by salary having count(salary)>=2;

select salary,count(salary)
from t11
where salary is not null
group by salary;

select salary,count(salary)
from t11
where salary is null
group by salary;
```

when the columns contains null data,
if use any aggregate function (count(), avg(), max(), min(), sum()) for
any column, which contains null data, then the aggregate function will not
consider the null values

when the column contains null data, if we use column with order by ASC,
the order by will give the result as " first it will keep all null values, then it
keep non null values in ascending order"

when the column contains null data, if we use column with order by DESC,
the order by will give the result as " first it will keep all non-null values in
descending order , then it keep null values at end"

when we use the column with group by clause , the it will keep null category result as always "0"

## how to check the null values in the table column

when we want to "null values" inside the a column, in MySQL we will use
a function called "isnull()"
if the column contains "null" value, then isnull() returns "1"
if the column contains "non-null" value, then isnull() returns "0"

if we want to see the total missing values or null values in a particular
column, then in MySQL we will use the following syntax:

```sql
select count(*)-count(column_name) from table_name;
```

when we want to retrieve the data from the column, if the column contains any null data, in place of null data, we want to show any default
value in the result, we will use a function called "ifnull()"

## example

```sql
select ifnull(id,10000) from t11;
```

when we working with null, in MySQL we will use a function called
"coalesce()", when we use coalesce() function with user-defined values,
always return "non-null" value

if coalesce() function got all are null values, it always return "null" as result

when we use the coalesce() function with column , it always takes one
by one value from the column, return the value based on the value what
it gets , if value is "null", then it will return "null", otherwise "non-null" value as result

## example

```sql
select null+10000;
select null*10000;
update t11 set salary=salary+10000;
select * from t11;
update t11
set salary=ifnull(salary,10000)+10000
where id is null;

delete from t11
where id is null;
select * from t11;
```

## example

```sql
select coalesce(null,null,null,1,2)
as result;
select coalesce(null)
as result;
```

## working with default and check constraints

by default , MySQL table fill column with "null" value, if we are not given
any value for the column while insertion

instead null value, we can give user-defined default value to the column,
in MySQL we will use a constraint called "default"

when we are inserting the any value into the column , if the column value
need to validate, where the value is correct value or incorrect value as
per the column, then we will use a constraint called "check"

## example

```sql
create table t22(
id int primary key
check(id>=100 and id<=10000),
firstname varchar(100) not null
default 'abc',
salary float check(salary>=10000)
default 10000);
```

## example

```sql
insert into t22(id)
values(100);
insert into t22(id)
values(-10);
insert into t22(id)
values(101);

select * from t22;
```

## example

```sql
alter table t22
modify id int auto_increment;
desc t22;
insert into t22(id) values(104);
select * from t22;
truncate table t22;
```

## example

```sql
create table
t23(id int primary key);
alter table t23
modify id int auto_increment;
desc t23;
```

when we are work with check constraint, the column of the table never
define with "auto_increment", if we define, MySQL will raise an error

when we define the column with not null constraint , the column never take "null" as default value ,when we are not given any value to the column while insertion, it always seeks for the value from the user for
insertion into the column

when we change the value of the auto_increment column using alter, it
change or reset the auto_increment column value, only when the table having any auto_increment column, otherwise it will not change or reset

when we want to give the "auto_increment" to the any column of the
table using alter, we can using following syntax:

```sql
alter table table_name modify column_name data type auto_increment
```

## example

```sql
use employee_fp1_2024;
drop table t23;
create table t23 (id int primary key);
desc t23;
alter table t23 auto_increment=1000;
alter table t23 modify id int
auto_increment;
insert into t23 values();
select * from t23;
```

in MySQL,

only one column can have the auto_increment and that column must
define with constraint either primary key or not null+unique or unique, never be not null constraint

when we define the column with auto_increment with unique, the column
will never take null values and even we given null values, it always takes
number as value
example:
```sql
create table t24
(id int unique auto_increment);
desc t24;
insert into t24 values(null);
select * from t24;
```

## foreign key

## master table or parent table

```sql
create table sample10(id int primary key,
firstname varchar(100) not null,
email varchar(100) not null);
```

## derived table or child table

```sql
create table enroll(
id int not null,
cid int not null,
cname varchar(100) not null,
foreign key(id) references
sample10(id) on update cascade
on delete cascade);
```

## inserting the data into sample10

```sql
insert into sample10
values(1,'a','a@gmail.com'),
(2,'b','b@gmail.com'),
(3,'c','c@gmail.com'),
(4,'d','d@gmail.com'),
(5,'e','e@gmail.com');
```

## retrieve the data from the Sample10

```sql
select * from sample10;
```

when we are inserting the data into "enroll", we always need to take
value for "id" , only always "any id of sample10 id column ", we not take any id value which is not present in the sample10, for enroll id column

## inserting the data into enroll

```sql
insert into enroll values(1, 1, 'python');
insert into enroll values(1, 2, 'python with sql'),
(2, 2, 'python with sql'),(2, 1, 'python');
select * from enroll;
```

## updating the data into enroll

```sql
update enroll set id=100
where id=1; <=== it will not run due to master table id column not have
"100" as value
update enroll set id=3
where id=1;
select * from enroll;
```

## update the sample10 table

```sql
update sample10 set id=100
where id=2;
select * from sample10;
select * from enroll;

update sample10 set id=300
where id=4;
update sample10 set firstname='abcd'
where id=1;
select * from enroll;
select * from sample10;

update sample10 set email='abcd@gmail.com'
where id=5;
update sample10 set id=2000
where id=5;
select * from enroll;
select * from sample10;
```

## delete the data from enroll

```sql
delete from enroll where id=100;
select * from enroll;
```

## delete the from the sample10

```sql
delete from sample10 where id=3;
select * from enroll;
select * from sample10;
```

## views in MySQL

views are called as "virtual tables"
views are not "physical tables"
views are created for another tables in MySQL
views are act as alias tables for "another table" with specific data
when we are retrieving the data from the table, it will scan entire table
to get the any data, instead of scanning the entire table for given query ,
we can scan the data only a part of data of the table, using "views"

when we want to create the view for any table in the MySQL, we will use
following syntax:

```sql
create view view_name as query;
```

when the table data is updated, view data is also updated
when the table data is deleted, view data is also deleted
when the new data is added into table, the data in view also can able
to get same new data
views are used to "get the data from table" based on the given query
the structure of the table and view , both are look like table, but in the view we can able retrieve data "What we need only using select"

## example

```sql
use employee_fp1_2024;
create view fp23 as select * from employee
where deptname='hr';
select * from fp23;
select firstname,lastname,salary from fp23
where salary>=60000 and salary<=140000;
```

## example

```sql
create or replace view fp23
as select firstname,lastname,salary from employee
where deptname='hr' order by salary desc limit 10;
select * from fp23;
select firstname,lastname,salary from fp23
where salary>=60000 and salary<=140000;
```

## example

```sql
create or replace view fp23 as
select * from employee where deptname='hr';
select * from fp23;
select * from employee where firstname='vikram';
update fp23 set salary=salary+10000;
delete from fp23 where firstname='vikram';
```

## example

```sql
create or replace view fp23 as
select id,firstname,lastname,salary,
joining_date,dob,blood_group,deptname,
deptid,gender,location,email,mobileno,designation
from employee where deptname='hr';
update fp23 set salary=salary-10000;
delete from fp23 where salary>=160000;
select max(salary) from fp23 where
deptname='hr';
update employee set salary=salary+10000
where deptname='hr';
```

## example

```sql
create or replace view fp23 as
select deptname,count(*) from employee
group by deptname;
select * from fp23;
update fp23 set deptname='xyz'
where deptname='abc';
```

when we want to drop the view or delete the view from the database
permanently, we will use the following syntax:

```sql
drop view view_name;
```

## example

```sql
drop view fp23;
select * from fp23;
```

## indexes in MySQL

index is a  "lookup table" for any table inside the database
indexes are used to "increase the performance of the select query"
in MySQL, we will have following types of indexes:

1. primary key index
2. regular index
3. unique index
4. composite index
5. full text index

## 1. primary key index

when we define the column with "primary key constraint", then the
column automatically gets a index called "primary key index"
for table, we can have only one "primary key index"

## 2. regular index

regular index refers a index
when we want to create a index for one column of table, then index is
called as "regular index"

## 3. composite index

when we create the index for "two or more columns" at a time , then index
is called as "composite index"

## 4. unique index

when we create the index for "one or more columns" using unique , then
the index is called as "unique index"

## 5. full text index

when we create the index for "one or more columns" using full text, then
then the index is called as "full text"

## in general indexes are two types

1. clustered index:
   1. primary key index

2. non-clustered index:
   1. regular index
   2. composite index
   3. unique index
   4. full text index

## example

create the table with name "Sample12"

```sql
use employee_fp1_2024;
create table sample12(id int primary key,
firstname varchar(100) not null,
lastname varchar(100) not null,
deptid int not null,
deptname varchar(100) not null,
salary float not null,
mobileno bigint not null);
```

when we want to show all indexes of the table, in MySQL we will use the
following syntax:

```sql
show indexes from table_name;
```

## example

```sql
desc sample12;
show indexes from sample12;
```

## create the regular index or index

to create the index in MySQL, we will use the following syntax:

```sql
create index index_name on table_name(column_names)
```

## example

```sql
create index i1 on sample12(deptid);
show indexes from sample12;
```

## create the unique index

to create the  unique index in MySQL, we will use the following syntax:

```sql
create  unique index index_name on table_name(column_names)
```

## example

```sql
create unique index i2 on sample12(deptid);
show indexes from sample12;
```

## create the composite index

in MySQL composite index means "Create the index for two or more
columns"
the composite index can be unique index
the composite index can be non-unique index
to create the composite index in mysql, we will use the following syntax:

```sql
create index index_name on table(col1,col2,col3,......coln)
```

or

```sql
create unique index_name on table(col1,col2,col3,......coln)
```

## example

```sql
create index i4 on
sample12(mobileno,deptname);
show indexes from sample12;
create unique index i5 on
sample12(mobileno,deptname);
show indexes from sample12;
```

## create the full text index

when we have the column are text type or categorical type or string type,
then in MySQL, we will use  the  "full text" as index for these type columns
or
when the  columns are defined with "varchar, char, text....." , then we will
preffered this index

to create the full text in MySQL, we will use the following syntax:

```sql
create fulltext index index_name on table_name(col1, col3,...coln);
```

## example

```sql
desc sample12;
create fulltext index i7 on sample12(firstname,
lastname);
show indexes from sample12;
```

when we create the index for any column, then index will uses the  following data structures to maintain internally, those are :

1. B-tree or B+ Tree (this is regular or primary or composite or unique index)
2. Inverted index (this is for full text index)

when we want to drop the any index of the table, in MySQL we will use
the following syntax:

```sql
drop index index_name on table_name
```

## example

```sql
drop index i1 on sample12;
drop index i2 on sample12;
show indexes from sample12;
```

if table is already created , we can also create the index, using alter command in MySQL without using create command
for this we will use the following syntax with alter:

```sql
alter table table_name add index index_name(column_name1,....);
alter table table_name add unique index index_name(column_name1,....);
alter table table_name add fulltext index index_name(column_name1,....);
```

## example

```sql
alter table sample12 add index i10(salary);
alter table sample12 add unique index i11(salary);
alter table sample12 add fulltext index i12(firstname);
show indexes from sample12;
```

in MySQL, we can create the index in the following  ways:

1. after table creation:
   1. using create index
   2. using alter
2. while creating the table using create command

creating the index while creating the table using create command, for this
we will use below syntax:

```sql
create table table_name(col1 type constrint, col2 type constraint, col3
type constrint, ..............coln type constrint,index index_name(col,col2......
coln))
```

```sql
create table table_name(col1 type constrint, col2 type constraint, col3
type constrint, ..............coln type constrint,unique index index_name(col,col2......
coln))
```

```sql
create table table_name(col1 type constrint, col2 type constraint, col3
type constrint, ..............coln type constrint,fulltext index index_name(col,col2......
coln))
```

## example

```sql
create table sample13(
id int, firstname varchar(100) not null,
lastname varchar(100) not null,
salary float not null,
mobileno bigint not null,
primary key(id), index i1(salary),
unique index i2(salary,mobileno));
show indexes from sample13;
```

indexes will not good performance "while we are doing the operations
like insert or update or delete on columns"
indexes will maintain "memory physically"
for table columns, we can not create too many indexes, we create indexes
for column wisely or based on requirement .

