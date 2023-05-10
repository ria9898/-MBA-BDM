# MBA-BDM

 ###### [Riya Singh - 22121003](https://github.com/ria9898)
 ###### [Akriti Toppo - 22121016](https://github.com/aakriti228)

### **INTRODUCTION:**

As a Business Analyst, We have been assigned the task of designing the database structure for a library management system. The purpose of a library management system is to help librarians manage their library's resources efficiently and provide library users with a seamless and easy-to-use experience.A well-designed database structure is essential to achieving these goals. The database should be able to store and manage all types of information related to the library, including information about books, users, borrowings, reservations, and transactions. It should be easy to use, secure, and capable of handling multiple users simultaneously.Additionally, the database structure should be able to generate reports and statistics on various aspects of the library management system, such as the most borrowed books, overdue books, and the number of registered users. This information can help librarians make informed decisions and improve the overall library experience for users.By having an efficient and easy-to-use database structure, librarians can spend less time on administrative tasks and more time focusing on providing quality services to their users. A well-designed database structure can make a significant impact on the library's overall efficiency and user experience.

### **Domain/Industry:** Library Management System

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
*  **Fine** Fine_ID , Borrow_ID ,Member_ID, Fine_Amount , Payment_Date


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





### **ENTITY RELATIONSHIP DIAGRAM FOR LIBRARY MANAGEMENT SYSTEM:** 
![ER DIAGRAMMM drawio](https://github.com/ria9898/-MBA-BDM/assets/126074369/8ae804b2-0b34-4751-a015-6b6f4e4a3e18)



### **CONVERTING THE ER DIAGRAM INTO TABLE:**

 **TABLE : Library**
 <br>
  
<pre>Library_ID         : INT PRIMARY KEY </pre>
<pre>Library_Name       : VARCHAR </pre>
<pre>Location           : VARCHAR </pre>
<pre>Contact_Number     : INT </pre>

EX:
| Library_ID |        Library_Name  | Location     |  Contact No. |
|------------|----------------------|--------------|--------------|
| 236746     |  Blossom Library     |Portofino     | 2362538846   |
| 124364     |  Grand Library       |Dasve         | 9786453427   |
| 844584     |  Osprey Library      |Hill View     | 1836715235   |
| 909767     |  Empress Library     |School Street | 9236834967   |
| 547748     |  Techno Library      |Thicket Street| 0993761361   |                  

<br>
<br>

**TABLE : Contact_Number** <br>

<pre>PHONE_NO_ID    : INT PRIMARY KEY </pre>
<pre>Library_ID     : VARCHAR </pre>
<pre>Contact_Number : VARCHAR </pre>

EX:
|PHONE_NO_ID|CUSTOMER_ID|PHONE_NUMBER|
|-----------|-----------|------------|
|     01    |  236746   |6775424587  |

<br>
<br>

**TABLE : ADDRESS**

<pre>ADDRESS_ID              : INT PRIMARY KEY </pre>
<pre>Vendor_ID               : INT FOREIGN KEY </pre>
<pre>Member_ID               : INT FOREIGN KEY </pre>
<pre>BUILDING_NO             : VARCHAR </pre>
<pre>FIRST_LINE              : VARCHAR </pre>
<pre>SECOND_LINE             : VARCHAR </pre>
<pre>PINCODE                 : VARCHAR </pre>

EX:
|ADDRESS_ID| Vendor_ID  |  Member_ID  |      BUILDING_NO       | FIRST_LINE| SECOND_LINE| PINCODE|
|----------|------------|-------------|------------------------|-----------|------------|--------|
|   01     |  737542    |   3246296   |         123            |  Main     |    St      |  600098|
<br>
<br>

**TABLE : Book**

<pre>Book_ID      : INT PRIMARY KEY </pre>
<pre>Book_Price   : DECIMAL </pre>
<pre>Book_Title   : VARCHAR </pre>
<pre>Book_Status  : VARCHAR </pre>

EX:
| Book_ID |        Book_Title         | BOOK Price |   BOOK Status |
|---------|---------------------------|------------|---------------|
| 23455   |  Research Methodology     |500/-       | Available     |
| 23545   |  Organizational Behaviour |980/-       | Not Available |
| 455478  |  Data Analysis            |1400/-      | Not Available |
| 345678  |  Financial Management     |400/-       | Available     |
| 455478  |  Marketing Analytics      |1200/-      | Not Available |


<br>
<br>

**TABLE : Author**

<pre>Author_ID        : VARCHAR PRIMARY KEY </pre>
<pre>Author_Name      : VARCHAR </pre>
<pre>Contact_Number   : INT FOREIGN KEY </pre>
<pre>Author Subject   : VARCHAR </pre>


EX:
| Author_ID |       Author_Name      | Contact No |  Author Subject |
|-----------|------------------------|------------|-----------------|
| 46587     |  C.R. Kothari          |284839283   |Research         |
| 12389     |  Stephen P. Robbins    |374828742   | Management      |
| 42308     |  Miachel S.            |273291247   |Computer Science |
| 32568     |  D.K. Goel             |284656289   | Finance         |
| 46878     | Mark Jeffery           |713627414   | Marketing       |


<br>
<br>

**TABLE : Publisher**

<pre>Publisher_ID    : INT PRIMARY KEY </pre>
<pre>Publisher_Name  : VARCHAR </pre>
<pre>Contact_Number  : INT FOREIGN KEY </pre>
<pre>Email           : VARCHAR FOREIGN KEY </pre>

EX:
|Publisher_ID  | Publisher_Name          | Contact_Number   | Email                        |
|--------------|-------------------------|------------------|------------------------------|
| 97757        |  Rishi Shah             |284839283         |rishi.shah@gmail.com          |
| 97875        |  Stephen lawrence       |374828742         |Lawrence.1212@gmail.com       |
| 97566        |  R.S Studio             |273291247         |r.sstudio@gmail.com           |
| 99643        |  Goel publishing House  |284656289         |goelhouse.publisher@gmail.com |
| 92467        |  Philips Kolter         |713627414         |kolterhouse@gmail.com         |
      
<br>
<br>

**TABLE : Vendor**

<pre>Vendor_ID      : INT PRIMARY KEY </pre>
<pre>Vendor_Name    : VARCHAR </pre>
<pre>Contact_Number : INT FORIGN KEY </pre>
<pre>Address        : VARCHAR FOREIGN KEY </pre>

EX:
|Vendor_ID     | Vendor_Name            | Contact_Number   | Address    |
|--------------|------------------------|------------------|------------|
| 463486       |  Alankar Shah          |813672738         |Nagpur      |
| 937583       |  Shankar Agarwal       |237628386         |Delhi       |
| 737542       |  Umakant Book Store    |768636732         |Gujarat     |
| 246291       | Crossword Enterprise   |328782731         |Mumbai      |
| 932468       | Khushwant Singh        |877672167         |Pune        | 
<br>
<br>

**TABLE :Member**

<pre>Member_ID          : INT PRIMARY KEY </pre>
<pre>Member_Name        : VARCHAR </pre>
<pre>Contact_Number     : INT FOREIGN KEY </pre>
<pre>Email              : VARCHAR </pre>
<pre>Address            : VARCHAR FOREIGN KEY </pre>
<pre>Date_of_Joining    : DATE </pre>

EX:
|Member_ID     | Member_Name       | Contact_Number   | Address    |   Email                     | Date_of_Joining  |
|--------------|-------------------|------------------|------------|-----------------------------|------------------|
|2728723       | Khushi Awasthi    |286289667         |Pune        | Khushi.awasthi@gmail.com    |   12-03-2020     |
|8786762       | Richa Singh       |128128629         |Delhi       | richi.rich@gmail.com        |   01-01-2021     |
|3863829       | Janet Joy         |989768611         |Patna       | janet.joy@yahoo.com         |   15-06-2020     | 
|3246291       | Anshu Singh       |912378982         |Gujarat     | acv.coc@yahoo.com           |   30-03-2022     |
|2332468       | Mayank Meet       |812167980         |Rajasthan   | mayankmeet.3456@gmail.com   |   10-10-2021     |

<br>
<br>

**TABLE : Admin**

<pre>Admin_ID       : INT PRIMARY KEY </pre>
<pre>Admin_Name     : VARCHAR </pre>
<pre>Contact_Number : INT FOREIGN KEY </pre>
<pre>Email          : VARCHAR FOREIGN KEY </pre>
<pre>Password       : VARCHAR  </pre>

EX:
|Admin_ID      | Admin_Name         | Contact_Number  | Email                    |  Password       |
|--------------|-------------------|------------------|--------------------------|-----------------|
|92371947      | Eesha Gupta       |9389137181        |eesha.gupta @yahoo.com    |    q1w2e3r      |
|08497482      | Radha Singh       |9237218189        |radha0909@gmail.com       |    o9i8u7y6     |
|82372891      | Rispa Maria       |9124563728        |rizpa.maria@yahoo.com     |    g5h6jfd3d    | 
|28311733      | Ansh Singh        |8669902203        |ansh.acv@gmail.com        |    xcv@34:e3    |
|98643612      | Akshat Kumar      |5688292914        |Akshat.qwerk@gmail.com    |    Life24*7     \ 
<br>
<br>

**TABLE :Employee**

<pre>Employee_ID      : INT PRIMARY KEY </pre>
<pre>Employee_Name    : VARCHAR </pre>
<pre>Contact_Number   : INT FOREIGN KEY </pre>


EX:
|Employee_ID   |Employee_Name         | Contact_Number   |
|--------------|----------------------|------------------|
|27482         |Gangu Ram             |9389137181        |
|10987         |shikhar Kumar         |9237218189        |
|90876         |Wilson                |9124563728        | 
|20673         |Santosh Kumar Singh   |8669902203        |
|60321         |Abhilash Shaji        |5688292914        |

<br>
<br>

**TABLE : Borrowing**

<pre>Borrow_ID     : INT PRIMARY KEY </pre>
<pre>Member_ID     : INT FOREIGN KEY </pre>
<pre>Book_ID       : INT FOREIGN KEY </pre>
<pre>Borrow_Date   : DATE  </pre>
<pre>Due_Date      : DATE  </pre>
<pre>Return_Date   : DATE  </pre>

EX:
|Borrow_ID     |  BOOK_ID     | Member_ID   | Borrow_date  | Due_date    | Return_date |
|--------------|--------------|-------------|--------------|-------------|-------------|
|834683        | 2736429      |2728723      | 14-02-2023   |  28-02-2023 | 03-03-2023  |
|934645        | 8272905      |9237191      | 20-03-2023   |  04-04-2023 | 03-04-2023  |
|196319        | 9612356      |1837199      | 25-02-2023   |  09-03-2023 | 12-03-2023  | 
|923299        | 1927010      |6432123      | 17-03-2023   |  31-03-2023 | 05-04-2023  |
|238912        | 9887882      |6428462      | 08-01-2023   |  22-01-2023 | 04-02-2023  | 

<br>
<br>

**TABLE : Fine**

<pre>Fine_ID            : INT PRIMARY KEY </pre>
<pre>Borrow_ID          : INT FOREIGN KEY </pre>
<pre>Fine_Amount        : DATE </pre>
<pre>Payment_Date       : DATE </pre>
<pre>Member_ID          : INT FOREIGN KEY </pre>


EX:
| Fine_ID | Borrow_ID | Fine_Amount | Payment_Date   |  Member_ID   |
|---------|-----------|-------------|----------------|--------------|
| 236746  | 834683    |  250        |  03-03-2023    |  2728723     |
| 124364  | 934645    |  50         |  03-04-2023    |  9237191     |
| 844584  | 238912    |  150        |  12-03-2023    |  6432123     |
| 909767  | 923299    |  400        |  05-04-2023    |  3764764     |  
| 547748  | 196319    |  750        |  04-02-2023    |  1837199     |


