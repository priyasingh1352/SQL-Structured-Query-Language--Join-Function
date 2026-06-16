create database college;
use college;

create table student(
id int primary key,
name varchar(50)
);

insert into student(id,name)
values
(101,"priya"),
(102,"anjali"),
(103,"ria"),
(104,"om");

create table course(
id int primary key,
course varchar(50));

insert into course(id,course)
values
(102,"english"),
(105,"python"),
(106,"DL"),
(107,"ML");


select* from student;
select*from course;

select*
from student
inner join course
on student.id = course.id;
             
             OR
select*from student as s
inner join course as c
on s.id = c.id;

select* from student as s
left join course as c
on s.id = c.id;

select* from student as s
right join course as c
on s.id = c.id;

select* from student as s
left join course as c
on s.id = c.id
union
select* from student as s
right join course as c
on s.id = c.id;

# Exclusive Join
# Exclusive Right Join

select* from student as s
right join course as c
on s.id = c.id
where c.id is null;

# Exclusive
# Exclusive Left Join
 
select* from student as s
right join course as c
on s.id = c.id
where c.id is null;

# Cross Join
select*
from student as s 
cross join course as c
on s.id = c.id;

select*from student;
update student set id = 111 where id = 102;

delete from student
where id = 104 ;

truncate table student;

alter 
