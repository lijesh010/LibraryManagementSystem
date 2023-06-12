# Library Management System
This project is a Library Management System that keeps track of all the information about books in the library, including their rental cost, status, and the total number of books available. It provides functionalities to manage branches, employees, customers, book issues, and returns.

## Database Setup
Create a new database named library to store the information.

Create the following tables within the library database:

### Branch
  ◾Branch_no (PRIMARY KEY)
  ◾Manager_Id
  ◾Branch_address
  ◾Contact_no
### Employee
  ◾Emp_Id (PRIMARY KEY)
  ◾Emp_name
  ◾Position
  ◾Salary
### Customer
  ◾Customer_Id (PRIMARY KEY)
  ◾Customer_name
  ◾Customer_address
  ◾Reg_date
### IssueStatus
  ◾Issue_Id (PRIMARY KEY)
  ◾Issued_cust (FOREIGN KEY, referencing Customer_id in CUSTOMER table)
  ◾Issued_book_name
  ◾Issue_date
  ◾Isbn_book (FOREIGN KEY, referencing isbn in BOOKS table)
### ReturnStatus
  ◾Return_Id (PRIMARY KEY)
  ◾Return_cust
  ◾Return_book_name
  ◾Return_date
  ◾Isbn_book2 (FOREIGN KEY, referencing isbn in BOOKS table)
### Books
  ◾ISBN (PRIMARY KEY)
  ◾Book_title
  ◾Category
  ◾Rental_Price
  ◾Status (yes if the book is available, no if the book is not available)
  ◾Author
  ◾Publisher
## Queries
### 1.Retrieve the book title, category, and rental price of all available books.
### 2.List the employee names and their respective salaries in descending order of salary.
### 3.Retrieve the book titles and the corresponding customers who have issued those books.
### 4.Display the total count of books in each category.
### 5.Retrieve the employee names and their positions for the employees whose salaries are above Rs.50,000.
### 6.List the customer names who registered before 2022-01-01 and have not issued any books yet.
### 7.Display the branch numbers and the total count of employees in each branch.
### 8.Display the names of customers who have issued books in the month of June 2023.
### 9.Retrieve book titles from the book table containing the category "history".
### 10.Retrieve the branch numbers along with the count of employees for branches having more than 5 employees.
