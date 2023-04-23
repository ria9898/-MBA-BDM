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
*  **Author** Author_ID , Author_Name , Contact_Number , Email
*  **Publisher** Publisher_ID , Publisher_Name , Contact_Number , Email
*  **Vendor** Vendor_ID , Vendor_Name , Contact_Number , Email
*  **Member** Member_ID , Member_Name , Contact_Number , Email , Address , Date_of_Joining
*  **Admin** Admin_ID , Admin_Name , Contact_Number , Email , Password
*  **Employee** Employee_ID , Employee_Name , Contact_Number , Email , Password
*  **Borrowing** Borrow_ID , Member_ID , Book_ID , Borrow_Date , Due_Date , Return_Date
*  **Fine** Fine_ID , Borrow_ID , Fine_Amount , Payment_Date

