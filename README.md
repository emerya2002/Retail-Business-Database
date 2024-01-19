# Retail-Business-Database

Project 1: Writing SQL Queries Using Oracle's SQL*Plus
Max Total: 15 points

Up to two students can work together on this project.

1.	Retail Business Database Schema
The following four tables are simplified from the tables for the Retail Business Management System project:

employees(eid, ename, telephone#)
customers(cid, cname, telephone#, visits_made, last_visit_date)
products(pid, pname, qoh, qoh_threshold, original_price, discnt_rate)
purchases(pur#, eid, pid, cid, ptime, qty, total_price)

•	Telephone numbers use this format: 607-777-1234 where the first 3 digits indicate the area code.
•	visits_made is the number of visits to the retail business a customer has made. 
•	last_visit_date is the date of the most recent visit made by a customer. Note that all visits made on the same day are counted as one visit. 
•	qoh is the quantity on hand.
•	qoh_threshold is the threshold for quantity on hand for adding supplies. 
•	original_price is the original price of a product. 
•	discnt_rate is the discount percentage over the original price of each product. 
•	ptime is the time when a purchase is made. 
•	qty is the quantity of product purchased.
•	total_price is the total dollar amount of each purchase. 
•	Each tuple in table purchases represents a purchase made by a customer for a product through an employee. eid, cid, pid and pur# are the primary keys of employees, customers, products, and purchases, respectively. 

2.	Preparation 
Save the provided project1.sql file in your harvey account. To run project1.sql in your Oracle account, do

SQL> start project1

Then check whether all tables are created correctly in your Oracle account.


3.	Statements
•	There are 15 statements in this project. 
•	You need to write a single SQL query for each statement. 
•	Each correct SQL query is worth 1 point. 
•	As tuples can be added, deleted, or updated, your queries must be correct for any tuples that could be different from the tuples given in project1.sql. 

I suggest that you first test each query individually and save each query in a different file (with extension .sql). After all queries have been tested to your satisfaction, you can run all the queries in sequence and save the entire session in a single spool file. For example, if you have query1.sql, ..., query15.sql, generate the spool file in your Oracle account as follows:

   SQL> set echo on
   SQL> spool project1.txt
   SQL> start query1
   .......
   SQL> start query15
   SQL> spool off

Convert your spool file into a single pdf file and turn it in through Gradescope as follows:
-	Remember to map each query to the corresponding statement on Gradescope. 
-	Write the B number and name of each team member at the beginning of the pdf file. 
-	Also, remember to list every team member on Gradescape when you submit it. 
-	Turn in just one pdf file per team.

The following are the 15 statements that you need to implement:

1.	Find the names and telephone#s of every customer who has visited the retail business at least twice, whose telephone# has an area code 315, and spent more than $100 in total. ( Is )

2.	Find the names and telephone#s of those customers who made at least one purchase with a total price of at least 50 dollars in the last 25 days (from the day your query is issued). 

3.	Find the pids and names of those products that are priced below 20 dollars (based on discount price) and are purchased through an employee named Peter. The discount price or sale price of a product is computed by original_price * (1 – discnt_rate).

4.	Find each purchase that involves an employee whose telephone number has the same area code as that of the customer who purchased a non-TV product. All attributes of qualified purchases should be returned.

5.	Find the purchase number (pur#) and ptime of each purchase. It is required that ptime be displayed in a format as illustrated by the following example: March 23, 2023, Friday 08:33:46. Furthermore, the results must be displayed in increasing ptime order.

6.	Find the eids of those employees whose telephone number has the same area code as that of at least one customer. Note that the customer may not necessarily have made a purchase from the employee. For this query, make sure that no duplicate results are returned, and you are not allowed to use “select distinct”. 

7.	Find the names of those employees who have not sold any product whose original price is $200 or higher. Use “not exists” to answer this query.

8.	Find the eids and names of those employees who have made sale to all the customers who have visited the retail business at least twice.

9.	Find those products that are purchased by customer c001 but not by customer c006. All attributes of qualified products should be returned.

10.	Find the cids of those customers who purchased at least one product that is also purchased by customer c003. Customer c003 should not be included in the result.

11.	Find the names of those customers who saved more than $100 in a single purchase (i.e., based on one record in the purchases table) from the original price of the product.

12.	Find the names of those customers who have made at least one purchase that has the highest total price among all purchases. Note that it is possible for multiple purchases to have the same highest total price.


13.	Find the cid and name of each customer as well as the number of different types of products purchased by the customer. 

14.	Find the cid and name of each customer who has visited the retail business the greatest number of times and display the total amount of money such a customer has spent at the retail business. Note that it is possible that multiple customers have visited the retail business for the (same) largest number of times.

15.	Find the names of the top three customers in terms of their spending at the retail business. For each such customer, also display the total amount of money the customer has spent. (The top three customers may have spent the same amount or different amounts of money. If more than three customers have the same highest expenditure at the retail store, return any one of those customers.)


![image](https://github.com/emerya2002/Retail-Business-Database/assets/95879915/61f915ed-05e8-4d50-b30b-c3dc892a9d59)
