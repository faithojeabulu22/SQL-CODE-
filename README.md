# SQL-CODE-

THIS IS A SERIES OF CODE, EXAMPLES PROJECT AND TUTORIAL I HAVE WORED ON 



JOIN
APPLYING JOIN IN A TABLE TO GET THE AVERAGE SALARY AND ORDERING IT  BY THE JOB TITLE 

select JobTitle, avg(Salary)
from [SQL tutorial ].dbo.EmployeeDemographics
inner join [SQL tutorial ].dbo.EmployeeSalary
     on EmployeeDemographics.EmployeeID =EmployeeSalary.EmployeeID

where JobTitle ='Salesman'
group by JobTitle ;


UNION // joining two tables together with their similar features
select EmployeeID,FirstName,Age
from [SQL tutorial ].dbo.EmployeeDemographics
union 
select  EmployeeID,JobTitle,Salary
from
[SQL tutorial ].dbo.EmployeeSalary
order by EmployeeID ;
