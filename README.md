# joins
text
---------------------CREATE DATABASE-------------------------------
create database compnay
---------------------ACTIVATE DATABASE------------------------------
use compnay
--------------------------CREATE TABLE EMPLOYEE-------------------------------
create table Employee(Id int primary key,Name varchar(20),Address varchar(20),salary money,dept_Id
int foreign key references Dpartment(Dept_Id))
--------------------------INAERT DATA IN TABLE EMPLOYEE--------------------------------------------
insert into Employee values
(1,'Ram','Noida',25000,1),
(2,'Mohan','Delhi',20000,2),
(3,'Shyam','Japan',30000,4),
(4,'Sita','Udisha',35000,5),
(5,'Gita','Noida',12000,NULL),
(6,'Sera','Haridwar',15000,NULL),
(7,'Satyam','Delhi',25000,3)

------------------------------CREATE TABLE DEPARTMENT------------------------------------------
create table Dpartment(Dept_Id int primary key,Dept_Name varchar(20))
-----------------------------INSERT DATA IN TABLE DEPARTMENT-------------------------
insert into Dpartment VALUES
(1,'IT'),
(2,'HR'),
(3,'ACCOUNT'),
(4,'SALES'),
(5,'IT')
---------------------DISPLAY RECORDS-------------------------
Select * from Employee

select * from Dpartment
-------------------------------------------INNER JOIN-----------------------------------------
select Name,Dept_Name from Dpartment a inner join Employee b on a.Dept_Id=b.dept_Id
-------------------------------------------LEFT JOIN------------------------------------------
select Name,Dept_Name from Dpartment a left join Employee b on a.Dept_Id=b.dept_Id
-------------------------------------------RIGHT JOIN-----------------------------------------
select Name,Dept_Name from Dpartment a right join Employee b on a.Dept_Id=b.dept_Id
-------------------------------------------FULL JOIN------------------------------------------
select Name,Dept_Name from Dpartment a full join Employee b on a.Dept_Id=b.dept_Id
-------------------------------------------CROSS JOIN-----------------------------------------
select Name,Dept_Name from Dpartment a cross join Employee b 

------------------------------------------SELF JOIN--------------------------------------------
create table EmployeeS(Id int primary key IDENTITY,Name varchar(20),Manager_Id
int)

insert into Employees values
('Ram',1),
('Mohan',2),
('Shyam',4),
('Sita',NULL),
('Gita',NULL)

select * from EmployeeS
select emp.Name Employee_Name , emp1.Name Manager_Name from EmployeeS emp  join EmployeeS emp1  on emp.Id=emp1.Manager_Id






























