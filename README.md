# Student Management System (Java)

This project is a **console-based Student Management System** implemented in Java.
It demonstrates key **Object-Oriented Programming (OOP)** concepts such as **inheritance, polymorphism, abstract classes, interfaces, method overloading/overriding, and modular design**.

The system allows users to add, search, update, delete, and view student records with automatic grade calculation based on marks.

---

## Objectives

* Apply **Inheritance** using an abstract parent class (`Person`) and a child class (`Student`).
* Implement **Interfaces** for CRUD operations (`RecordActions`).
* Demonstrate **Polymorphism**:

  * *Static Polymorphism* → Method Overloading (`calculateGrade()` in `Student`).
  * *Dynamic Polymorphism* → Method Overriding (`displayInfo()` in `Student`, CRUD in `StudentManager`).
* Use **Collections (HashMap)** to efficiently store and manage students.
* Provide a **menu-driven system** to handle student operations dynamically.

---

## Class Hierarchy

1. **Person (abstract class)**

   * Fields: `name`, `email`
   * Abstract Method: `displayInfo()`

2. **Student (extends Person)**

   * Fields: `rollNo`, `course`, `marks`, `grade`
   * Methods:

     * `calculateGrade(double marks)`
     * `calculateGrade(int marks)` (overloaded)
     * Overrides `displayInfo()`

3. **RecordActions (interface)**

   * Methods:

     * `addStudent(Student s)`
     * `deleteStudent(int rollNo)`
     * `updateStudent(int rollNo, Student s)`
     * `searchStudent(int rollNo)`
     * `viewAllStudents()`

4. **StudentManager (implements RecordActions)**

   * Uses `HashMap<Integer, Student>` for storage
   * Implements all CRUD methods with duplicate roll number prevention

5. **StudentManagementSystem (Main Class)**

   * Provides **menu-driven interface**
   * Uses `Scanner` for dynamic input
   * Demonstrates add, update, delete, search, and view operations

---

## Data Types Used

* `String` → name, email, course
* `int` → rollNo
* `double` → marks
* `HashMap<Integer, Student>` → storage and management of student records

---

##  Features

* Add new student records dynamically.
* Prevents duplicate roll numbers.
* Search students by roll number.
* Update existing student details.
* Delete student records.
* View all students with details and grades.
* Automatic **grade calculation** based on marks:

  * `A` → 90 and above
  * `B` → 75–89
  * `C` → 50–74
  * `D` → below 50

---

## Example Menu Flow

```
--- Student Management Menu ---
1. Add Student
2. View All Students
3. Search Student
4. Update Student
5. Delete Student
6. Exit
Enter choice: 1
Enter Roll No: 101
Enter Name: Riya
Enter Email: riya@mail.com
Enter Course: BCA
Enter Marks: 88
Student added successfully!
```

---

## How to Run

1. Save the code in a file named `StudentManagementSystem.java`.
2. Compile the program:

   ```bash
   javac StudentManagementSystem.java
   ```
3. Run the program:

   ```bash
   java StudentManagementSystem
   ```
4. Use the menu to perform different operations.

---

