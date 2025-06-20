# Student-Management-System

OVERVIEW
--------
This project is a Java-based console application designed to handle student-related information, including:

- Basic personal information

- Academic exam results

- Fee details and payment structure

OBJECT-ORIENTED FEATURES USED
-----------------------------
1. Interface: Abstraction via IStudent interface
2. Inheritance:
   - Exam extends Student
   - Fee extends Exam
3. Method Overriding: Fee overrides display() to show all student info
4. Polymorphism: Uniform interface for student input and display


CLASS & INTERFACE STRUCTURE

INTERFACE: IStudent
-------------------
Methods:
- void student_input(): For inputting basic student details
- void display(): For displaying student information

CLASS: Student (implements IStudent)
------------------------------------
Fields:
- int system_id
- String name
- String course
- int sem

Methods:
- student_input(): Inputs student data
- display(): Outputs student data
- getSystemId(): Getter for ID

CLASS: Exam (extends Student)
-----------------------------
Fields:
- int sub1, sub2, sub3, sub4, sub5
- int total
- float per
- String grade, result

Methods:
- examinput(): Inputs subject marks and calculates total, percentage, grade, and result
- examDisplay(): Displays exam result and statistics

CLASS: Fee (extends Exam)
-------------------------
Fields:
- float tuitionFee
- float examFee
- float totalFee

Methods:
- feeInput(): Inputs tuition and exam fee
- feeDisplay(): Displays fee details
- display(): OVERRIDDEN to show Student + Exam + Fee info

MAIN CLASS: studentManagement
-----------------------------
Responsibilities:
- Manages the program flow
- Presents menu to user
- Maintains list of students using ArrayList<Fee>
- Routes input to appropriate methods

OPTIONS LIST:
1. Add Student
2. View Students (basic info only)
3. Add Exam Marks
4. View Exam Result
5. Add Fee Details
6. View Fee Structure
7. View All Details by System ID
8. Exit
