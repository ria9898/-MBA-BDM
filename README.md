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


**TABLE : Library**

| Library_ID |        Library_Name  | Location     |  Contact No. |
|------------|----------------------|--------------|--------------|
| 236746     |  Blossom Library     |Portofino     | 2362538846   |
| 124364     |  Grand Library       |Dasve         | 9786453427   |
| 844584     |  Osprey Library      |Hill View     | 1836715235   |
| 909767     |  Empress Library     |School Street | 9236834967   |
| 547748     |  Techno Library      |Thicket Street| 0993761361   |



**TABLE : Book**

| Book_ID |        Book_Title         | BOOK Price |   BOOK Status |
|---------|---------------------------|------------|---------------|
| 23455   |  Research Methodology     |500/-       | Available     |
| 23545   |  Organizational Behaviour |980/-       | Not Available |
| 455478  |  Data Analysis            |1400/-      | Not Available |
| 345678  |  Financial Management     |400/-       | Available     |
| 455478  |  Marketing Analytics      |1200/-      | Not Available |


**TABLE : Author**

| Author_ID |       Author_Name      | Contact No |  Author Subject |
|-----------|------------------------|------------|-----------------|
| 46587     |  C.R. Kothari          |284839283   |Research         |
| 12389     |  Stephen P. Robbins    |374828742   | Management      |
| 42308     |  Miachel S.            |273291247   |Computer Science |
| 32568     |  D.K. Goel             |284656289   | Finance         |
| 46878     | Mark Jeffery           |713627414   | Marketing       |


**TABLE : Publisher**

|Publisher_ID  | Publisher_Name          | Contact_Number   | Email                        |
|--------------|-------------------------|------------------|------------------------------|
| 97757        |  Rishi Shah             |284839283         |rishi.shah@gmail.com          |
| 97875        |  Stephen lawrence       |374828742         |Lawrence.1212@gmail.com       |
| 97566        |  R.S Studio             |273291247         |r.sstudio@gmail.com           |
| 99643        |  Goel publishing House  |284656289         |goelhouse.publisher@gmail.com |
| 92467        |  Philips Kolter         |713627414         |kolterhouse@gmail.com         |
      
        
  **TABLE : Vendor**

|Vendor_ID     | Vendor_Name            | Contact_Number   | Address    |
|--------------|------------------------|------------------|------------|
| 463486       |  Alankar Shah          |813672738         |Nagpur      |
| 937583       |  Shankar Agarwal       |237628386         |Delhi       |
| 737542       |  Umakant Book Store    |768636732         |Gujarat     |
| 246291       | Crossword Enterprise   |328782731         |Mumbai      |
| 932468       | Khushwant Singh        |877672167         |Pune        |      
 
 
 
  **TABLE : Member**      
        
|Member_ID     | Member_Name       | Contact_Number   | Address    |   Email                     | Date_of_Joining  |
|--------------|-------------------|------------------|------------|-----------------------------|------------------|
|2728723       | Khushi Awasthi    |286289667         |Pune        | Khushi.awasthi@gmail.com    |   12-03-2020     |
|8786762       | Richa Singh       |128128629         |Delhi       | richi.rich@gmail.com        |   01-01-2021     |
|3863829       | Janet Joy         |989768611         |Patna       | janet.joy@yahoo.com         |   15-06-2020     | 
|3246291       | Anshu Singh       |912378982         |Gujarat     | acv.coc@yahoo.com           |   30-03-2022     |
|2332468       | Mayank Meet       |812167980         |Rajasthan   | mayankmeet.3456@gmail.com   |   10-10-2021     |
 


  **TABLE : Admin**      
        
|Admin_ID      | Admin_Name         | Contact_Number  | Email                    |  Password       |
|--------------|-------------------|------------------|--------------------------|-----------------|
|92371947      | Eesha Gupta       |9389137181        |eesha.gupta @yahoo.com    |    q1w2e3r      |
|08497482      | Radha Singh       |9237218189        |radha0909@gmail.com       |    o9i8u7y6     |
|82372891      | Rispa Maria       |9124563728        |rizpa.maria@yahoo.com     |    g5h6jfd3d    | 
|28311733      | Ansh Singh        |8669902203        |ansh.acv@gmail.com        |    xcv@34:e3    |
|98643612      | Akshat Kumar      |5688292914        |Akshat.qwerk@gmail.com    |    Life24*7     |
 
   
 
  **TABLE : Employee**      
        
|Employee_ID   |Employee_Name         | Contact_Number   |
|--------------|----------------------|------------------|
|27482         |Gangu Ram             |9389137181        |
|10987         |shikhar Kumar         |9237218189        |
|90876         |Wilson                |9124563728        | 
|20673         |Santosh Kumar Singh   |8669902203        |
|60321         |Abhilash Shaji        |5688292914        |
    
    
 **TABLE : Borrowing**      
        
|Borrow_ID     |  BOOK_ID     | Member_ID   | Borrow_date  | Due_date    | Return_date |
|--------------|--------------|-------------|--------------|-------------|-------------|
|834683        | 2736429      |2728723      | 14-02-2023   |  28-02-2023 | 03-03-2023  |
|934645        | 8272905      |9237191      | 20-03-2023   |  04-04-2023 | 03-04-2023  |
|196319        | 9612356      |1837199      | 25-02-2023   |  09-03-2023 | 12-03-2023  | 
|923299        | 1927010      |6432123      | 17-03-2023   |  31-03-2023 | 05-04-2023  |
|238912        | 9887882      |6428462      | 08-01-2023   |  22-01-2023 | 04-02-2023  |   
       

 **TABLE :Fine**

| Fine_ID | Borrow_ID | Fine_Amount | Payment_Date   |
|---------|-----------|-------------|----------------|
| 236746  | 834683    |  250        |  03-03-2023    |  
| 124364  | 934645    |  50         |  03-04-2023    |
| 844584  | 238912    |  150        |  12-03-2023    |
| 909767  | 923299    |  400        |  05-04-2023    |
| 547748  | 196319    |  750        |  04-02-2023    |

            
        
**SQL Command**     
        
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
         
             
