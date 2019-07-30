# MySQL_50_questions
大陸經典MySQL 50道練習題

首先先建立以下table

--1.學生表

Student(SId,Sname,Sage,Ssex)

--SId 學生編號,Sname 學生姓名,Sage 出生年月,Ssex 學生性別
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



--2.課程表

Course(CId,Cname,TId)

--CId 課程編號,Cname 課程名稱,TId 教師編號
```
create table Course(CId varchar(10),Cname nvarchar(10),TId varchar(10));
insert into Course values('01' , '語文' , '02');
insert into Course values('02' , '數學' , '01');
insert into Course values('03' , '英語' , '03')
```

--3.教師表

Teacher(TId,Tname)

--TId 教師編號,Tname 教師姓名
```
create table Teacher(TId varchar(10),Tname varchar(10));
insert into Teacher values('01' , '張三');
insert into Teacher values('02' , '李四');
insert into Teacher values('03' , '王五')
```

--4.成績表

SC(SId,CId,score)

--SId 學生編號,CId 課程編號,score 分數
```
create table SC(SId varchar(10),CId varchar(10),score decimal(18,1));
insert into SC values('01' , '01' , 80);
insert into SC values('01' , '02' , 90);
insert into SC values('01' , '03' , 99);
insert into SC values('02' , '01' , 70);
insert into SC values('02' , '02' , 60);
insert into SC values('02' , '03' , 80);
insert into SC values('03' , '01' , 80);
insert into SC values('03' , '02' , 80);
insert into SC values('03' , '03' , 80);
insert into SC values('04' , '01' , 50);
insert into SC values('04' , '02' , 30);
insert into SC values('04' , '03' , 20);
insert into SC values('05' , '01' , 76);
insert into SC values('05' , '02' , 87);
insert into SC values('06' , '01' , 31);
insert into SC values('06' , '03' , 34);
insert into SC values('07' , '02' , 89);
insert into SC values('07' , '03' , 98)
```

#練習題目

1. 查詢" 01 "課程比" 02 "課程成績高的學生的信息及課程分數

1.1 查詢同時存在" 01 "課程和" 02 "課程的情況

1.2 查詢存在" 01 "課程但可能不存在" 02 "課程的情況(不存在時顯示為null )

1.3 查詢不存在" 01 "課程但存在" 02 "課程的情況

2. 查詢平均成績大於等於60 分的同學的學生編號和學生姓名和平均成績

3. 查詢在SC 表存在成績的學生信息

4. 查詢所有同學的學生編號、學生姓名、選課總數、所有課程的總成績(沒成績的顯示為null )

4.1 查有成績的學生信息

5. 查詢「李」姓老師的數量 

6. 查詢學過「張三」老師授課的同學的信息 

7. 查詢沒有學全所有課程的同學的信息 

8. 查詢至少有一門課與學號為" 01 "的同學所學相同的同學的信息 

9. 查詢和" 01 "號的同學學習的課程完全相同的其他同學的信息 

10. 查詢沒學過"張三"老師講授的任一門課程的學生姓名 

11. 查詢兩門及其以上不及格課程的同學的學號，姓名及其平均成績 

12. 檢索" 01 "課程分數小於60，按分數降序排列的學生信息

13. 按平均成績從高到低顯示所有學生的所有課程的成績以及平均成績

14. 查詢各科成績最高分、最低分和平均分：

    以如下形式顯示：課程ID，課程name，最高分，最低分，平均分，及格率，中等率，優良率，優秀率
    及格為>=60，中等為：70-80，優良為：80-90 ，優秀為：>=90 
    要求輸出課程號和選修人數，查詢結果按人數降序排列，若人數相同，按課程號升序排列

15. 按各科成績進行排序，並顯示排名， Score 重複時保留名次空缺

15.1 按各科成績進行排序，並顯示排名， Score 重複時合併名次

16. 查詢學生的總成績，並進行排名，總分重複時保留名次空缺

16.1 查詢學生的總成績，並進行排名，總分重複時不保留名次空缺

17. 統計各科成績各分數段人數：課程編號，課程名稱，[100-85]，[85-70]，[70-60]，[60-0] 及所佔百分比

18. 查詢各科成績前三名的記錄

19. 查詢每門課程被選修的學生數 

20. 查詢出只選修兩門課程的學生學號和姓名 

21. 查詢男生、女生人數

22. 查詢名字中含有「風」字的學生信息

23. 查詢同名同性學生名單，並統計同名人數

24. 查詢1990 年出生的學生名單

25. 查詢每門課程的平均成績，結果按平均成績降序排列，平均成績相同時，按課程編號升序排列

26. 查詢平均成績大於等於85 的所有學生的學號、姓名和平均成績 

27. 查詢課程名稱為「數學」，且分數低於60 的學生姓名和分數 

28. 查詢所有學生的課程及分數情況（存在學生沒成績，沒選課的情況）

29. 查詢任何一門課程成績在70 分以上的姓名、課程名稱和分數

30. 查詢不及格的課程

31. 查詢課程編號為01 且課程成績在80 分以上的學生的學號和姓名

32. 求每門課程的學生人數 

33. 成績不重複，查詢選修「張三」老師所授課程的學生中，成績最高的學生信息及其成績

34. 成績有重複的情況下，查詢選修「張三」老師所授課程的學生中，成績最高的學生信息及其成績

35. 查詢不同課程成績相同的學生的學生編號、課程編號、學生成績 

36. 查詢每門功成績最好的前兩名

37. 統計每門課程的學生選修人數（超過5 人的課程才統計）。

38. 檢索至少選修兩門課程的學生學號 

39. 查詢選修了全部課程的學生信息

40. 查詢各學生的年齡，只按年份來算 

41. 按照出生日期來算，當前月日< 出生年月的月日則，年齡減一

42. 查詢本週過生日的學生

43. 查詢下週過生日的學生

44. 查詢本月過生日的學生

45. 查詢下月過生日的學生
