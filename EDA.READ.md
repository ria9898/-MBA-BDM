
# PROBLEM STATEMENTS

 **LIST THE NAME OF THE BOOKS WHICH ARE AVAILABLE IN THE LIBRARY**
 --SQL QUERY
 SELECT Book_Title, Book_Status FROM Book WHERE Book_Status = 'Available';
 

 **retrieve the library id of the libraries whose name contains the word "name" and their id contains the digit "4"**
 --SQL QUERY
  SELECT Library_ID FROM library WHERE Library_ID LIKE '%4%' AND  Library_Name LIKE '%o%';


**Retrieve all members from the Member table, sorted by their date of joining.**
-- SQL QUERY
SELECT * FROM Member ORDER BY Date_of_Joining;


 **Retrieve all employees from the Employee table, sorted by their employee ID in ascending order**
 -- SQL QUERY
 SELECT * FROM Employee ORDER BY Employee_ID ASC;
 
**Retrieve the member ID and payment date from the Fine table where the fine amount is greater than 50.**
-- SQL QUERY
 SELECT Member_ID, Payment_Date FROM Fine WHERE Fine_Amount > 50;
 
 **Count the number of borrowing records where the return date is greater than the due date.**
 -- SQL QUERY
 SELECT COUNT(*) FROM Borrowing WHERE Return_date > Due_date;
 
 **Retrieve the vendor name and member name from either "Pune" or "Gujarat"**
 -- SQL QUERY
 SELECT Vendor_Name, Member_Name
FROM Vendor
JOIN Member ON Vendor.Address = Member.Address
WHERE Vendor.Address IN ('Pune', 'Gujarat');

** Calculate the total sum of all fine amounts in the Fine table.**
-- SQL QUERY
SELECT SUM(Fine_Amount) AS Total_Fine_Amount FROM Fine;

**Calculate the average fine amount in the Fine table.**
-- SQL QUERY
SELECT AVG(Fine_Amount) AS Average_Fine FROM Fine;

**Retrieve the percentage of vendors and members grouped by their address in ascending order**
-- SQL QUERY
SELECT 'Vendor' AS Address, COUNT(*) *100.0/(SELECT COUNT(*) FROM Vendor) AS Percentage FROM Vendor GROUP BY Address UNION ALL SELECT 'Member' AS Address, COUNT(*)*100.0/(SELECT COUNT(*) FROM Member) AS Percentage FROM Member GROUP BY Address ORDER BY Address;


**Retrieve the payment date and total fine amount in descending order, limiting the results to only the highest amount.**
-- SQL QUERY
SELECT Payment_Date AS Month, SUM(Fine_Amount) AS Total_Fine 
FROM Fine
GROUP BY Payment_Date
ORDER BY Total_Fine DESC 
LIMIT 1;

**Retrieve the borrowing ID, member name, and book title with their respective IDs.**
-- SQL QUERY
SELECT Borrowing.Borrow_ID, Member.Member_Name, Book.Book_Title
FROM Borrowing
INNER JOIN Member ON Borrowing.Member_ID = Member.Member_ID
INNER JOIN Book ON Borrowing.Book_ID = Book.Book_ID;

**Show the price of Books**
-- SQL QUERY
select Book_Title,Book_Price from book;
![image](https://github.com/ria9898/-MBA-BDM/assets/125997110/eaa5d791-8d34-4fcb-97ec-5d28b203ced6)

-- Show the Fine Amt. from Borrow ID
select  Borrow_ID,Fine_Amount  from fine;
![image](https://github.com/ria9898/-MBA-BDM/assets/125997110/4934fd5b-381a-40ea-886c-2074970a678e)

-- 



