# LeetCode Problems #


----------

1. Database
	
	
	> Easy

		627. Swap Salary
		update salary set sex = if(sex = 'm', 'f', 'm')
		
		596. Classes More Than 5 Students
		select c.class from courses c group by c.class having count(distinct c.student) > 4
		#tips：一个学生同选一门课无效(distinct)

		595. Big Countries
		select name, population, area from World where(area > 3000000 or population > 25000000)

		620. Not Boring Movies
		select * from cinema where(description != 'boring' and id%2 = 1) order by rating desc

		197. Rising Temperature
		SELECT w1.Id FROM Weather w1, Weather w2 WHERE w1.Temperature > w2.Temperature AND DATEDIFF(w1.RecordDate, w2.RecordDate) = 1;

		196. Delete Duplicate Emails
		delete p1 from Person p1, Person p2 where p1.Email=p2.Email and p1.Id>p2.Id

		183. Customers Who Never Order
		SELECT Name as Customers FROM Customers c WHERE c.Id NOT IN (SELECT CustomerId FROM Orders o)

		182. Duplicate Emails
		select Email from Person group by email having count(Email) > 1

		181. Employees Earning More Than Their Managers
		select e.Name as Employee from employee e,employee m where e.managerid=m.id and e.salary>m.salary
		#将表作为两个镜像别名表来对比

		176. Second Highest Salary
		select ifnull((select Distinct Salary from Employee order by Salary desc limit 1,1), null) as SecondHighestSalary

		175. Combine Two Tables
		select p.FirstName, p.LastName, a.City, a.State from Person p left join Address a on p.PersonId = a.PersonId



2. Algorithms

3. Shell