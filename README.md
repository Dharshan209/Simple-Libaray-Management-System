## Library Management System with MySQL and JFrame in NetBeans

This document provides an overview of the Library Management System developed using MySQL and JFrame in NetBeans. It details the system's functionality, installation instructions, and database structure.

**Features:**

* **Book Management:**
    * Add, remove, and update book entries.
    * View a list of available books with filter options.
    * Search for specific books by title, author, or category.
* **Staff Management:**
    * Add, remove, and update staff information.
    * View a list of all staff members.
    * Edit staff contact details.
* **Admin Login:**
    * Secure access to system settings and management tools.
    * Manage user accounts and access permissions.

**System Flow:**

1. **Launch the application:** Run the `Main.java` file after setting up the project in NetBeans.
2. **Login (Admin):** Provide valid credentials to access administrative features.
3. **Dashboard:** View key metrics like available books, staff count, and quick access buttons for management functionalities.
4. **Book Management:**
    * **Add Book:** Enter book details (title, author, category, copies) and add to the database.
    * **Remove Book:** Select a book from the list and remove it from the database.
    * **Update Book:** Edit existing book information and save changes.
    * **View Books:** Browse through a list of available books, filter by category, or search by title/author.
5. **Staff Management:**
    * **Add Staff:** Enter staff details (name, phone number) and add to the database.
    * **Remove Staff:** Select a staff member from the list and remove them from the database.
    * **Edit Staff:** Modify existing staff information and save changes.
    * **View Staff:** View a list of all staff members with their contact details.
6. **Admin Settings (Accessible after login):**
    * Manage user accounts and roles.
    * Configure system settings like database connection and display parameters.
    * View system logs and audit trails.

**Database Structure:**

The system utilizes three primary tables:

* **admin:** Stores user credentials for system administration (user_id, name, password, phone number).
* **books:** Holds information about available books in the library (book_id, name, category, copies).
* **staff:** Maintains data on staff members (staff_id, name, phone number).

**Note:** The provided SQL statements in the initial query illustrate table creation, sample data insertion, and data retrieval for demonstration purposes. These functionalities are handled dynamically within the system's Java code.

**Installation and Setup:**

1. Clone the repository.
2. Import the project into NetBeans.
3. Configure the database connection within the Java code (refer to project comments for connection details).
4. Run the `LoginPage.java` file.

**MySQL CODE**
**copy this code mysql workbench or commandpromtline**

use libaray;
create table admin
(user_id varchar(50) primary key,
name varchar(30),
password varchar(30),
phn_number varchar(10));
insert into admin values('dharshan@123','dharshan','Dharshan@209','9345450064');
create table books
(Book_id varchar(50) primary key,
name varchar(30),
Category varchar(30),
copies int(10));
insert into books values('H001','Advance java','java','10');
create table staff
(staff_id varchar(50) primary key,
name varchar(30),
phn_number varchar(10));
insert into staff values('S001','dharshan','9345450064');
select * from admin;
select * from books;
select * from staff;

**Additional Notes:**

* This is a basic documentation structure. Feel free to customize and expand it with screenshots, detailed usage instructions, troubleshooting tips, and contribution guidelines.
* Ensure to update the README with any future updates or features added to the system.

I hope this comprehensive README provides a clear understanding of the Library Management System's functionalities and usage. Feel free to leave any questions or feedback for further improvement of the documentation.

