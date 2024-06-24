CREATE DATABASE DepartamentDB
USE DepartamentDB

create table Departments(
	Id int not null unique identity(1,1),
	Name nvarchar(150) not null,
	MaxEmployeeCount int check(MaxEmployeeCount >= 10 and MaxEmployeeCount <= 50)
)

create table Positions(
	Id int not null unique identity(1,1),
	Name nvarchar(50) not null
)

create table Employees(
	Id int not null unique identity(1,1),
	Name nvarchar(60) default 'Employee Name',
	SurName nvarchar(70) default 'Employee Surname',
	Salary decimal(18,2) check(Salary >= 500 and Salary <= 12000)
)

Insert into Employees(Salary)
values
(2000)

Select * from Employees