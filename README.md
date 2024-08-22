# Library Management System

## Overview
This project is a **Library Management System** written in C++. It allows library administrators to manage books and student records efficiently. The system supports functionalities such as adding, modifying, deleting, and searching for books and student records. Additionally, it includes features for issuing and returning books.

## Features
### Book Management
- **Add New Book**: Allows the admin to add new books to the library’s inventory.
- **Display All Books**: Lists all the books available in the library.
- **Search Book**: Search for a book by its number and display its details.
- **Modify Book**: Update the details of a specific book.
- **Delete Book**: Remove a book from the library’s inventory.

### Student Management
- **Add New Student**: Allows the admin to register new students in the system.
- **Display All Students**: Lists all the students registered in the library.
- **Search Student**: Search for a student by their admission number and display their details.
- **Modify Student**: Update the details of a specific student.
- **Delete Student**: Remove a student's record from the system.

### Book Issue/Return
- **Issue Book**: Allows a student to issue a book from the library. The system will check if the book is available and update the records accordingly.
- **Return Book**: Handles the return of issued books and calculates any late return fines.

### Admin Menu
The admin has access to a menu that allows them to:
- Manage books and student records.
- Issue and return books.
- Perform the above-listed tasks with ease.

### Password Protection
- The system is protected by a password that must be entered before accessing the admin menu.

## Classes
### `book`
- **Attributes**:
  - `bno`: Book number.
  - `quant`: Quantity of the book.
  - `bname`: Book name.
  - `aname`: Author's name.
  - `pname`: Publication name.
- **Methods**:
  - `createb()`: Create a new book record.
  - `showb()`: Display a book's details.
  - `showlist()`: Display book details in list form.
  - `assignbno(int x)`: Assign a book number based on the number of existing records.
  - `set_q()`: Decrease the quantity of the book by one.
  - `reset_q()`: Increase the quantity of the book by one.
  - `quantity()`: Return the current quantity of the book.
  - `retbno()`: Return the book number.

### `student`
- **Attributes**:
  - `admno`: Admission number.
  - `name`: Student's name.
  - `bno`: Book number of the issued book.
  - `token`: Indicates if a book is issued (1) or not (0).
- **Methods**:
  - `creates()`: Create a new student record.
  - `shows()`: Display a student's details.
  - `showlist()`: Display student details in list form.
  - `settoken(int x)`: Set the token when a book is issued.
  - `resettoken()`: Reset the token when a book is returned.
  - `retbno()`: Return the book number of the issued book.

## File Operations
- **Books File**: All book records are stored in `book1.bin`.
- **Students File**: All student records are stored in `student.bin`.

## Notes
- The default password for the system is `"0000"`. This can be changed directly in the source code.
- The system prompts the user for input and provides necessary feedback for each action.
- Fine for late book returns is calculated at `Rs. 1` per day after a 15-day period.
