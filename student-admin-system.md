# Assignment: Student Administration System

## Learnings

* Data Structures
* Lists and Dicts
* Text based user interfaces

## Description

You are tasked with building a simple student administration system for teachers to manage their students. The system will store student records, including their personal information and subjects they are taking. Teachers will be able to perform various operations, such as adding new students, removing existing students, and listing all students in the system.

## Requirements

### 1: Design the data structure

* Each student record should be represented as a dictionary.
* The dictionary should contain the following key-value pairs:

	* "name": The name of the student (string).
	* "email": The email address of the student (string).
	* "full_name": The full name of the student (string).
	* "subjects": A list of subjects the student is taking (list of strings).

### 2: Implement the following functionalities

a) Adding a student:

The teacher should be able to add a new student to the system.
The system should prompt the teacher to enter the student's name, email address, full name, and subjects they are taking.

The student record should be stored in an appropriate data structure.

b) Removing a student:

The teacher should be able to remove an existing student from the system.
The system should prompt the teacher to enter the name of the student they want to remove.
If the student is found in the system, they should be removed from the data structure.
If the student is not found, an appropriate message should be displayed.

c) Listing all students:

The teacher should be able to view a list of all the students in the system.
The system should display each student's name, email address, full name, and subjects they are taking.
The student records should be displayed in a clear and organized manner.

### 3: Create a user-friendly interface

* The system should provide a user-friendly interface for teachers to interact with.
Teachers should be able to easily navigate through different functionalities and perform the required operations.
The interface should display clear instructions and provide appropriate prompts to guide the teacher's actions.