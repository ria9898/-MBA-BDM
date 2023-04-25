# MBA-BDM

 ###### [Riya Singh - 22121003](https://github.com/ria9898)
  ###### [Akriti Toppo - 22121016](https://github.com/aakriti228)

### **INTRODUCTION:**

As a Business Analyst, We have been assigned the task of designing the database structure for a library management system. The purpose of a library management system is to help librarians manage their library's resources efficiently and provide library users with a seamless and easy-to-use experience.A well-designed database structure is essential to achieving these goals. The database should be able to store and manage all types of information related to the library, including information about books, users, borrowings, reservations, and transactions. It should be easy to use, secure, and capable of handling multiple users simultaneously.Additionally, the database structure should be able to generate reports and statistics on various aspects of the library management system, such as the most borrowed books, overdue books, and the number of registered users. This information can help librarians make informed decisions and improve the overall library experience for users.By having an efficient and easy-to-use database structure, librarians can spend less time on administrative tasks and more time focusing on providing quality services to their users. A well-designed database structure can make a significant impact on the library's overall efficiency and user experience.

### **Domain/Industry:** Library Management System

#### **Entities:**

1. Library
2. Books
3. Author
4. Publisher
5. Vendor
6. Member
7. Admin
8. Empolyee
9. Borrowing
10. Fine

#### **Attributes:**
*  **Library** Library_ID , Library_Name , Location , Contact_Number 
*  **Book** Book_ID , Book_Price , Book_Title , Book_Status
*  **Author** Author_ID , Author_Name ,Author_Subject ,Contact_Number 
*  **Publisher** Publisher_ID , Publisher_Name , Contact_Number , Email
*  **Vendor** Vendor_ID , Vendor_Name , Contact_Number , Address
*  **Member** Member_ID , Member_Name , Contact_Number , Email , Address , Date_of_Joining
*  **Admin** Admin_ID , Admin_Name , Contact_Number , Email , Password
*  **Employee** Employee_ID , Employee_Name , Contact_Number
*  **Borrowing** Borrow_ID, Member_ID , Book_ID , Borrow_Date , Due_Date , Return_Date
*  **Fine** Fine_ID , Borrow_ID , Fine_Amount , Payment_Date


### **ER DIAGRAM:** 
![ER DIAGRAM](https://user-images.githubusercontent.com/126074369/234172039-74566170-1ba1-412d-befe-305ea053733c.png)

**TABLE : Book**

| Book_ID |        Book_Title         | BOOK Price |   BOOK Status |
|---------|---------------------------|------------|---------------|
| 23455   |  Research Methodology     |500/-       | Available     |
| 23545   |  Organizational Behaviour |980/-       | Not Available |
| 455478  |  Data Analysis            |1400/-      | Not Available |
| 345678  |  Financial Management     |400/-       | Available     |
| 455478  |  Marketing Analytics      |1200/-      | Not Available |


**TABLE : WISHLIST**

|WISHLIST_ID | DATE_CREATED |
|------------|--------------|


**TABLE : PROMOTION**

|PROMOTION_ID | START_DATE | END_DATE | DISCOUNT_PERCENTAGE |
|-------------|------------|----------|---------------------|
      
         |        Book   | Author         |Publisher        |                                
         | ------------- |:-------------: | -----------:    |
         | Book ID       |  Author_ID     |Publisher ID     |
         | Book Title    |   Author Name  |Publisher Name   |
         | Book Price    |   Contact No   |Contact No       |
         |Book Status    | Author Subject |Email ID         |
 
         
         
         
         
|     Vendor    | Member             |Admin             |                                
| ------------- |:-------------:     | -----:           |
| Vendor ID     |  Member_ID         |Admin  ID         |
|   Vendor Name |  Member Name       |  Admin   Name    |
| Contact No    |   Contact No       |Contact No        |
|Address        | Email ID           |Email ID          |
|               |Date of Joining     |  Password        |

    
 





    
    
    
    
    
    
    
         |        Book   | Author         |Publisher        |                                
         | ------------- |:-------------: | -----------:    |
         | Book ID       |  Author_ID     |Publisher ID     |
         | Book Title    |   Author Name  |Publisher Name   |
         | Book Price    |   Contact No   |Contact No       |
         |Book Status    | Author Subject |Email ID         |
 
 


    
    
    
    
    
    
              +------------+          +------------+       +-------------- +
              |    Book    |          |   Author   |       |  Publisher    |
              +------------+          +------------+       +-------------- +
              | Book_ID    |          | Author_ID  |       | Publisher ID  |
              | Book_Title |<---+     | Author_Name|<--+   | Publisher Name|
              | Book_Price |          | Contact No |       | Contact No    |
              | Book_Status|          | Email ID   |       | Email  ID     |
              +------------+          +------------+       +---------------+
                      |                      |                    |
                      |                      |                    |
                      |                      |                    |
                      |                      |                    |
              +------------+      +------------+                  |
              |    Vendor  |      |  Category  |                  |
              +------------+      +------------+                  |
              | Vendor ID  |      | Category_I |<-----------------+
              | Vendor Name|      | Category_N |
              | Contact No |      |            |
              | Address    |      |            |
              +------------+      +------------+

                      |                     |
                      |                     |
                      |                     |
                      |                     |
              +------------+     +------------+
              |   Member   |     |    Admin   |
              +------------+     +------------+
              | Member_ID  |     | Admin_ID   |
              | Member_Nam |      | Admin_Name |
              | Contact_Nu |      | Contact_Nu |
              | Email      |      | Email      |
              | Address    |      | Password   |
              | Date_of_Jo |      +------------+
              +------------+

                      |
                      |
                      |
                      |
              +------------+
              |   Employee |
              +------------+
              | Employee_I|
              | Employee_N|
              | Contact_N |
              | Email     |
              | Password  |
              +------------+

                      |
                      |
                      |
                      |
              +------------+
              |  Borrowing |
              +------------+
              | Borrow_ID |
              | Borrow_Dat|
              | Due_Date  |
              | Return_Dat|
              | Fine      |
              | Member_ID |
              | Book_ID   |
              +------------+

                      |
                      |
                      |
                      |
              +------------+
              |    Fine    |
              +------------+
              | Fine_ID    |
              | Borrow_ID  |
              | Fine_Amount|
              | Payment_Dat|
              +------------+

        
        
  CREATE TABLE Library (
         Library_ID INT PRIMARY KEY,
         Library_Name VARCHAR(255),
         Location VARCHAR(255),
         Contact_Number VARCHAR(20)
     );
 CREATE TABLE Book (Book_ID INT PRIMARY KEY,
         Book_Price DECIMAL(10, 2),
         Book_Title VARCHAR(255),
         Book_Status VARCHAR(10)
     );

 CREATE TABLE Author (
         Author_ID INT PRIMARY KEY,
         Author_Name VARCHAR(255),
         Contact_Number VARCHAR(20),
         Email VARCHAR(255)
     );


 CREATE TABLE Publisher (
         Publisher_ID INT PRIMARY KEY,
         Publisher_Name VARCHAR(255),
         Contact_Number VARCHAR(20),
         Email VARCHAR(255)
     );

 CREATE TABLE Vendor (
         Vendor_ID INT PRIMARY KEY,
         Vendor_Name VARCHAR(255),
         Contact_Number VARCHAR(20),
         Email VARCHAR(255)
     );

 CREATE TABLE Member (
         Member_ID INT PRIMARY KEY,
         Member_Name VARCHAR(255),
         Contact_Number VARCHAR(20),
         Email VARCHAR(255),
         Address VARCHAR(255),
         Date_of_Joining DATE
     );

mysql> CREATE TABLE Admin (
         Admin_ID INT PRIMARY KEY,
         Admin_Name VARCHAR(255),
         Contact_Number VARCHAR(20),
         Email VARCHAR(255),
         Password VARCHAR(255)
     );

mysql> CREATE TABLE Employee (
    ->     Employee_ID INT PRIMARY KEY,
    ->     Employee_Name VARCHAR(255),
    ->     Contact_Number VARCHAR(20),
    ->     Email VARCHAR(255),
    ->     Password VARCHAR(255)
    -> );

 CREATE TABLE Borrowing (
         Borrow_ID INT PRIMARY KEY,
         Member_ID INT,
         Book_ID INT,
         Borrow_Date DATE,
         Due_Date DATE,
         Return_Date DATE,
         FOREIGN KEY (Member_ID) REFERENCES Member(Member_ID),
         FOREIGN KEY (Book_ID) REFERENCES Book(Book_ID)
     );

 CREATE TABLE Fine (
         Fine_ID INT PRIMARY KEY,
         Borrow_ID INT, 
         Fine_Amount DECIMAL(10, 2),
         Payment_Date DATE,
         FOREIGN KEY (Borrow_ID) REFERENCES Borrowing(Borrow_ID)
         
             
