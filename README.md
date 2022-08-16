# SQL-CODE-

THIS IS A SERIES OF CODE, EXAMPLES PROJECT AND TUTORIAL I HAVE WORED ON 



---JOIN
APPLYING JOIN IN A TABLE TO GET THE AVERAGE SALARY AND ORDERING IT  BY THE JOB TITLE 

select JobTitle, avg(Salary)
from [SQL tutorial ].dbo.EmployeeDemographics
inner join [SQL tutorial ].dbo.EmployeeSalary
     on EmployeeDemographics.EmployeeID =EmployeeSalary.EmployeeID

where JobTitle ='Salesman'
group by JobTitle ;


---UNION // joining two tables together with their similar features
select EmployeeID,FirstName,Age
from [SQL tutorial ].dbo.EmployeeDemographics
union 
select  EmployeeID,JobTitle,Salary
from
[SQL tutorial ].dbo.EmployeeSalary
order by EmployeeID ;



---ALIASING // changing your table name or a column name making it more readable 


select demo.EmployeeID, demo.FirstName, demo.LastName, sal.JobTitle, ware.Age


from [SQL tutorial ].dbo.EmployeeDemographics as demo
left join [SQL tutorial ].dbo.EmployeeSalary as sal
    on demo.EmployeeID =sal.EmployeeID
left join  [SQL tutorial ].dbo.WareHouseEmployeeDemographics as ware 
     on demo.EmployeeID = ware.EmployeeID
     
     
     
  --- PARTITIONING BY 
  
select  FirstName, LastName,Gender,Salary,
COUNT(Gender)  over (partition by Gender) as totalgeneder 

from [SQL tutorial ].dbo.EmployeeDemographics as demo
join [SQL tutorial ].dbo.EmployeeSalary as sal
    on demo.EmployeeID =sal.EmployeeID
