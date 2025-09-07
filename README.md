# Student Management System (Java + JDBC)

A simple console-based Java application to manage student records using JDBC and MySQL.

## Features
- Add a new student  
- View all students  
- Update student details  
- Delete student records  

## Technologies
- Java  
- JDBC (MySQL Connector)  
- MySQL Database  

## Setup
1. Clone this repository:
   ```bash
   git clone <https://github.com/SinaliW/student-JDBC>
   ```
2. Create a MySQL database:
   ```sql
   CREATE DATABASE studentsdata;
   USE studentsdata;

   CREATE TABLE students (
       id INT AUTO_INCREMENT PRIMARY KEY,
       name VARCHAR(100) NOT NULL,
       age INT NOT NULL,
       grade VARCHAR(10) NOT NULL
   );
   ```
3. Update your database credentials in `DatabaseConnection.java`:
   ```java
   private static final String URL = "jdbc:mysql://localhost:3306/studentsdata";
   private static final String USER = "root";
   private static final String PASSWORD = "";
   ```
4. Add the MySQL Connector JAR inside the `lib/` folder.  
5. Compile and run:
   ```bash
   javac -cp "lib/mysql-connector-java-8.1.0.jar;." -d bin src/*.java
   java -cp "lib/mysql-connector-java-8.1.0.jar;bin" Main
   ```

## Usage
When running, the console will display a menu:
```
=== Student Management System ===
1. Add Student
2. View Students
3. Update Student
4. Delete Student
5. Exit
```
Follow the prompts to manage student records.
