# StudentGrades

A simple command-line application for managing student records. Built as a first-year Python project demonstrating fundamental programming concepts.

## Project Overview

This system allows you to:
- Add new student records
- View all students
- Search for students by ID or name
- Update student information
- Delete student records
- Calculate individual student results (marks, percentage, grade)
- View class statistics (average marks, highest marks, lowest marks, pass/fail counts)

All data is stored in memory during runtime (not persistent).

## Project Structure

```
student-record-management/
├── main.py                 # Entry point of the application
├── student.py              # Student class definition
├── student_manager.py      # StudentManager class for CRUD operations
├── utilities.py            # Helper functions for validation and display
├── README.md               # This file
└── .gitignore              # Git ignore file
```

## How to Run

### Prerequisites
- Python 3.6 or higher
- Terminal/Command Prompt

### Steps to Run

1. **Navigate to the project folder:**
   ```bash
   cd student-record-management
   ```

2. **Run the program:**
   ```bash
   python main.py
   ```
   
   Or on macOS/Linux:
   ```bash
   python3 main.py
   ```

3. **Follow the on-screen menu** to manage student records.

## Menu Options

```
1. Add Student
   - Enter student ID, name, age, course, and marks
   - System checks for duplicate IDs

2. View All Students
   - Displays all students currently in the system
   
3. Search Student
   - Search by Student ID or Name
   - Partial name search is supported

4. Update Student
   - Find a student by ID
   - Update any of their information (name, age, course, marks)

5. Delete Student
   - Remove a student record by ID

6. Calculate Student Result
   - View marks, percentage, grade, and pass/fail status
   - Grading scale:
     * A: 80-100 (PASS)
     * B: 70-79  (PASS)
     * C: 60-69  (PASS)
     * D: 50-59  (PASS)
     * F: 0-49   (FAIL)

7. Display Class Statistics
   - Total number of students
   - Average marks
   - Highest marks
   - Lowest marks
   - Number of passing students
   - Number of failing students

8. Exit
   - Close the application
```

## Sample Usage

### Adding a Student
```
Main Menu:
1. Add Student
2. View All Students
3. Search Student
4. Update Student
5. Delete Student
6. Calculate Student Result
7. Display Class Statistics
8. Exit

Enter your choice (1-8): 1

--- Add New Student ---
Enter Student ID: 101
Enter Name: Alice Johnson
Enter Age: 19
Enter Course: Computer Science
Enter Marks (0-100): 85

✓ Student added successfully!
```

### Viewing All Students
```
Enter your choice (1-8): 2

--- All Students ---
ID: 101 | Name: Alice Johnson | Age: 19 | Course: Computer Science | Marks: 85
ID: 102 | Name: Bob Smith | Age: 20 | Course: Mathematics | Marks: 92
```

### Searching for a Student
```
Enter your choice (1-8): 3

--- Search Student ---
Search by (1) ID or (2) Name? Enter 1 or 2: 1
Enter Student ID: 101

✓ Student found:
ID: 101 | Name: Alice Johnson | Age: 19 | Course: Computer Science | Marks: 85
```

### Calculating Result
```
Enter your choice (1-8): 6

--- Calculate Student Result ---
Enter Student ID: 101

Student: Alice Johnson
ID: 101
Age: 19
Course: Computer Science
Marks: 85
Percentage: 85.0%
Grade: A
Status: PASS
```

### Viewing Statistics
```
Enter your choice (1-8): 7

--- Class Statistics ---
==================================================
           CLASS STATISTICS
==================================================
Total Students: 2
Average Marks: 88.50
Highest Marks: 92
Lowest Marks: 85
Passing Students: 2
Failing Students: 0
==================================================
```

## Input Validation

The program validates all user inputs:
- **Student ID**: Must be a positive integer
- **Name**: Cannot be empty, letters and spaces only
- **Age**: Must be between 15 and 25
- **Marks**: Must be between 0 and 100
- **Menu Choice**: Must be between 1 and 8

If invalid input is provided, the program will display an error message and ask you to try again.

## Concepts Used

### Python Fundamentals
- Variables, data types, basic syntax

### Object-Oriented Programming
- `Student` class: Represents individual student
- `StudentManager` class: Manages all records

### Data Structures
- **Lists**: Store multiple Student objects
- **Sets**: Track unique student IDs
- **Dictionaries**: Store student information and statistics

### Control Flow
- if/elif/else statements for decisions
- while loops for validation and main menu loop
- for loops for iteration through students

### Functions
- Input validation functions
- CRUD operation functions
- Statistics calculation functions

### Operators
- Comparison operators: `==`, `>=`, `<=`, `>`, `<`
- Logical operators: `and`, `or`, `not`
- Membership operators: `in` (for checking student IDs)
- Arithmetic operators: `+`, `/` (for calculations)
- Assignment operators: `=`, `+=`

### Modules
- Organized code into separate files
- Imported functions and classes using `from` and `import`

## Common Errors and How to Fix Them

### Error: "ModuleNotFoundError: No module named 'student_manager'"
**Cause**: You're not in the correct directory
**Fix**: Make sure all files are in the same folder, and you run `python main.py` from that folder

### Error: "ValueError: invalid literal for int()"
**Cause**: You entered text when a number was expected
**Fix**: Enter only numbers for Student ID, Age, and Marks

### Error: "A student with this ID already exists"
**Cause**: You tried to add a student with an ID that's already in use
**Fix**: Use a different, unique Student ID

### Error: Program doesn't display anything
**Cause**: Python file might not have the correct code
**Fix**: Make sure all files were copied correctly without any errors

## Troubleshooting

1. **Program won't start**: Ensure you have Python 3.6+ installed
2. **Menu doesn't appear**: Check that main.py is in the same folder as other files
3. **"No module" error**: Verify all files are in the project folder
4. **Input validation keeps failing**: Follow the constraints (ID > 0, Age 15-25, Marks 0-100)

## Notes

- All data is stored **in memory** and will be lost when you close the program
- No database is used (as per requirements)
- This is a **terminal-based application** (no GUI)
- Designed for first-year Python students

## Author's Notes

This project demonstrates:
- How to organize code into multiple files (modularity)
- How to design simple classes for data representation
- How to validate user input
- How to build a menu-driven application
- How to work with lists, sets, and dictionaries

---
