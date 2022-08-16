# SQL-CODE-

THIS IS A SERIES OF CODE, EXAMPLES PROJECT AND TUTORIAL I HAVE WORED ON 



JOIN
APPLYING JOIN IN A TABLE TO GET THE AVERAGE SALARY AND ORDERING IT  BY THE JOB TITLE 

select JobTitle, avg(Salary)
from [SQL tutorial ].dbo.EmployeeDemographics
inner join [SQL tutorial ].dbo.EmployeeSalary
     on EmployeeDemographics.EmployeeID =EmployeeSalary.EmployeeID

where JobTitle ='Salesman'
group by JobTitle
