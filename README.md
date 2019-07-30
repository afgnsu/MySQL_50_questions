# MySQL_50_questions
大陸經典MySQL 50道練習題

首先先建立以下table

```
create table Student(SId varchar(10),Sname varchar(10),Sage datetime,Ssex varchar(10));
insert into Student values('01' , '趙雷' , '1990-01-01' , '男');
insert into Student values('02' , '錢電' , '1990-12-21' , '男');
insert into Student values('03' , '孫風' , '1990-05-20' , '男');
insert into Student values('04' , '李雲' , '1990-08-06' , '男');
insert into Student values('05' , '周梅' , '1991-12-01' , '女');
insert into Student values('06' , '吳蘭' , '1992-03-01' , '女');
insert into Student values('07' , '鄭竹' , '1989-07-01' , '女');
insert into Student values('09' , '張三' , '2017-12-20' , '女');
insert into Student values('10' , '李四' , '2017-12-25' , '女');
insert into Student values('11' , '李四' , '2017-12-30' , '女');
insert into Student values('12' , '趙六' , '2017-01-01' , '女');
insert into Student values('13' , '孫七' , '2018-01-01' , '女')
```

create table Course(CId varchar(10),Cname nvarchar(10),TId varchar(10));
insert into Course values('01' , '語文' , '02');
insert into Course values('02' , '數學' , '01');
insert into Course values('03' , '英語' , '03')
