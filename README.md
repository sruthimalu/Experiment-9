# Experiment-9

Order by and Group by clause

1.Create table employee with fields Code , name , dob , designation , salary.

2.Display code, name, and designation in descending order of the name.

3.Create table deposit with fields baccno , branch_name , amount .

4.Give branch name and details of deposit table

#1

create table employee(code varchar(25), name varchar(100),dob date, designation varchar(25),salary varchar(20));

insert into employee(code, name, dob, designation, salary) values('emp1','varun', '1998-02-02','manager',40000), ('emp2','ram', '1997-07-07','professor',35200),('emp3','ravi','1998-04-03','clerk',35000);

#2

select code, name, designation from employee order by name desc;

#3

CREATE TABLE Deposit(

    baccno BIGINT(30),

    branch_name VARCHAR(60),

    amount FLOAT

);

INSERT INTO Deposit(baccno, branch_name, amount)

VALUES

(381134,'Thekkekara',200000),

(382006,'Thekkekara',280000),

(383889,'Thekkekara',100000),

(384000,'Thekkekara',26500),

(385000,'Thekkekara',20500);

#4

SELECT branch_name,COUNT(baccno),SUM(amount) FROM Deposit GROUP BY branch_name;

