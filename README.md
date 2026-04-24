Student Management System Database (SQL Project)

Project Overview

This project is a relational database system designed to manage students, courses, departments, and enrollments. It helps store, organize, and analyze academic data efficiently.

Problem Statement

Educational institutions often struggle with tracking student performance, course registration, and departmental distribution. This database solves these issues by centralizing data and enabling easy analysis.

Database Schema Description

The database consists of the following tables:
- Students: stores student personal details
- Courses: stores course information
- Enrollments: links students to courses and records grades
- Departments: stores department information

SQL Schema Example
CREATE TABLE students (
    student_id INT PRIMARY KEY,
    name VARCHAR(100),
    age INT,
    department VARCHAR(50)
);

CREATE TABLE courses (
    course_id INT PRIMARY KEY,
    course_name VARCHAR(100),
    lecturer VARCHAR(100)
);

CREATE TABLE enrollments (
    enrollment_id INT PRIMARY KEY,
    student_id INT,
    course_id INT,
    grade INT,
    FOREIGN KEY (student_id) REFERENCES students(student_id),
    FOREIGN KEY (course_id) REFERENCES courses(course_id)
);

6. Key Analysis / Queries
- Top performing students based on average grade
- Students not enrolled in any course
- Department with highest number of students
- Average grade per course

Tools Used
- MySQL / SQL Server
- Excel (for initial data cleaning)
- Power BI or Pivot Tables (for analysis if applicable)

