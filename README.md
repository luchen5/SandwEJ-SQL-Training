# SandwEJ-SQL-Training

SandwEJ is SQL training project to create, designing database according to the descriptions

# Description

SandwEJ is a sandwich shop that is rising in its popularity due to selling sandwiches with unique taste and appearance. The manager, having to known you for a long time, ask you for a favor to build a database for recording sandwich sales and ingredient purchases.

Every staff that hired by SandwEJ have a task to serve customers who wants to buy sandwiches and purchase ingredients from vendor. Every staff must be following the procedures to become a staff, which are:

•	Every staff hired must have their personal information recorded. The information needed are the staff’s name, gender, salary, and phone number. Every staff has an identification code with the following format:

![image](https://github.com/user-attachments/assets/7df2fc9b-4fa0-4896-8f38-b97fb7166bdd)
 
•	Every chef hired must have their information recorded. The information needed are the chef’s name, and experience. Every chef has an identification code with the following format:

![image](https://github.com/user-attachments/assets/4a5f9cce-60bd-42cc-88fe-060cd60f9383)

•	Every customer that wants to make a purchase must already completed their personal information. The information needed are the customer’s name, gender, date of birth (DoB), and phone number. Every customer has an identification code with the following format:
 
 ![image](https://github.com/user-attachments/assets/b4104e48-d1ac-4b41-9d9d-b3aeaee4a58a)

•	Every vendor that wants to sell their ingredient must already completed their information. The information needed are the vendor’s name, address, phone number, and email. Every vendor has an identification code with the following format:
 
 ![image](https://github.com/user-attachments/assets/28174476-e7a7-419f-bd73-3cac55c2a7a1)

•	Every ingredient must have several information. They are the ingredient’s name and price. Every ingredient has an identification code with the following format:

![image](https://github.com/user-attachments/assets/bd67ab31-0029-4bfe-ae34-3407c2f674cd)
 
•	Every sandwich sold by SandwEJ have several information. They are the sandwich’s name, sauce, and price. Every sandwich has an identification code with the following format:

![image](https://github.com/user-attachments/assets/b11fd7d1-ae90-42fe-b2ab-3e907360715f)
 
•	Every purchase transaction made with the supplier has several information. They are the staff who made the purchase, the vendor who sold the ingredients, the transaction’s date, ingredients purchased, and the quantity of each kind of ingredient. Every purchase transaction has an identification code with the following format:
 
![image](https://github.com/user-attachments/assets/893b99d5-8d9b-43ef-a4de-8d6cfe2ac36d)

•	Customer can purchase more than one kind of sandwich in every transaction.
•	Every sales transaction made by the customer have several information. They are the staff who served the customer, the customer who made the purchase, the chef who cooked the sandwiches, the transaction’s date, sandwiches sold, and the quantity of each kind of sandwich. Every sales transaction has an identification code with the following format:

![image](https://github.com/user-attachments/assets/d19a4768-44cd-49b2-a252-d1499cecdc76)
  
•	Staff can buy more than one ingredient in every transaction.

Notes: Make the following constraints:
•	Customer gender must be either “Male” or “Female” (without quote).
•	Customer phone number must be exactly 12 characters.
•	Vendor email with the following format:
o	Contains “@” and “.com” (without quote).
o	“@” must not be at the beginning.
o	“.com” must be at the end.
o	“@” and “.com” must not be placed beside each other.
o	Valid emails example:
	john@gmail.com
	a@a.com
	haytam@kenway.com
o	Invalid emails example:
	anonymcom
	@blyke.com
	sandwej@e.commail
	sandwej@.com
•	Sandwich price must be between 5000 and 500000.
•	Sales date must be at least today or before.
•	Purchase date must be at least today or before.

Now, based on the requirements specified by SandwEJ manager before, you are asked to do several things:
a.	Create Entity Relationship Diagram to maintain sales and purchase transactions.
b.	Create a database system using DDL syntax that relevant with sales and purchase transactions. The database system must include database and tables with the required procedures.
c.	Create query using DML syntax to fill the tables in database systems with data based on the following conditions:
•	Master table must be filled with more than or equals 10 data.
•	Transaction table must be filled with more than or equals 15 data.
•	Transaction detail table must be filled with more than or equals 25 data.
•	For the Chef table, the chef experience column must have the following data:
![image](https://github.com/user-attachments/assets/2a916844-fb7e-42f1-88aa-d86b602ccae2)


d.	Create query using DML syntax to simulate the transactions process for sales and purchase transactions. 
Note: DML syntax to fill database and DML syntax to simulate the transactions process should be a different query.
e.	To support database management process in SandwEJ, the manager asked you to provide some query that resulting important data. The requirements that asked from him are:
1.	Display CustomerName, CustomerPhoneNumber, where the transaction happened in 2019 and the sum of the quantity greater than 3.

2.	Display StaffName, Transaction Count (obtained from the count of sales), where the staff served customer whose name started with T and customer’s birthdate month is greater than 9.

3.	Display Chef Name (obtained from chef name in lower case), Average Sandwich Per Transaction (obtained from the average of sales quantity) for every chef whose experience is not beginner, and sum of its cooked sandwich is greater than 3.

4.	Display Vendor Code (obtained from the last three digit of vendor id), Vendor Name (obtained from vendor name, where all word ‘Company’ replaced by ‘Co.’), Minimum Item Price (obtained from the minimum of ingredient price), and Maximum Item Price (obtained from the maximum of ingredient price) for every vendor whose email ended with ‘@gmail.com’ and vendor’s name is composed of three words.

5.	Display Staff Nickname (obtained from the first and the last character of staff name), StaffSalary for staff who’s served female customer, and the salary of the staff is higher than the average salary.
(alias subquery)

6.	Display CustomerName, Customer Age (obtained from the distance between current date and customer dob in year), SandwichName, Quantity (obtained from sales quantity added by ‘ Piece(s)’ at the end) where the sales quantity is smaller than 5, and the customer age is greater than the average of all customer age.
(alias subquery)

7.	Display Price (obtained from sandwich price added by the minimum price of all sandwich), and SandwichName for every sandwich which name has two words and the sum of its sales quantity between 5 and 25, sorted ascendingly.
(alias subquery)
8.	Display StaffName, Staff Salary (obtained from staff salary added by ‘Rp. ’ at the front, with numbers after point (.xx) ignored), Gender (obtained from the first letter of staff gender) for every staff whose salary is between the minimum and average of male staff’s salary.
(alias subquery)

9.	Create a view called ‘Staff Sales Statistic’ which display StaffName, SandwichName, Sales Count (obtained from the count of sales occurred), Sales Total (obtained from the sum of sales quantity) where the sandwich name composed of at least two words, and the sum of the sales quantity is greater than 1.

10.	Create a view called ‘Vendor Statistic’ which display VendorName, Price Range (obtained from the maximum of ingredient price minus minimum of ingredient price), Minimum Item Purchase (obtained from the minimum of purchase quantity), Maximum Item Purchased (obtained from the maximum of purchase quantity) for every vendor whose address does not contain the word ‘Gold’, and the Price Range is greater than 0.

Notes: Every column result which has no name should be named, according to the requirement (case sensitive, and space usage mattered)

File that must be collected:
1.	Entity Relationship Diagram (.vsdx, .png)
2.	Query to create the database system. (.sql)
3.	Query to insert data into tables. (.sql)
4.	Query to simulate the transactions processes. (.sql)
5.	Query to answer the 10 cases. (.sql)




