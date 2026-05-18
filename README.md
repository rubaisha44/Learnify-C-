# Learnify - Online Course Enrollment System

## Overview

Learnify is a Windows Forms desktop application developed in C# that serves as a course enrollment management system. The system allows students to browse available courses, select additional learning materials, and enroll with applicable discounts based on their education level. Teachers can log in to manage their courses, add new courses, edit existing ones, toggle registration status, and view enrolled students.

## Features

### Student Features
- User registration and login
- Browse courses by category and difficulty level
- Select multiple courses for enrollment
- Choose additional materials (Quick Guide, Self Learning Bundle)
- Automatic discount calculation (40% for undergraduate, 20% for graduate students)
- View enrollment receipt

### Teacher Features
- Teacher login authentication
- Add new courses
- Edit existing courses
- Open or close course registration
- View list of enrolled students for each course

### General Features
- Data persistence using JSON files
- Sample data generation for first-time use
- User-friendly Windows Forms interface

## Technologies Used

- **Language:** C#
- **Framework:** .NET Framework 4.8
- **UI Technology:** Windows Forms
- **Data Serialization:** System.Text.Json
- **Documentation:** Doxygen (XML comments)

## Project Structure
Learnify/
├── Course.cs # Course class with validation
├── Student.cs # Student class
├── Teacher.cs # Teacher class
├── CourseData.cs # Data persistence management
├── frmMain.cs # Main student dashboard
├── frmLogin.cs # Login form
├── frmRegister.cs # Registration form
├── frmTeacherDashboard.cs # Teacher management interface
├── frmTeacherLogin.cs # Teacher login form
├── frmCourseEdit.cs # Add/Edit course form
├── frmDisplay.cs # Display receipt form
├── Program.cs # Application entry point
├── App.config # Application configuration
└── Learnify.csproj # Project file



## Installation and Setup

### Prerequisites
- Windows operating system
- .NET Framework 4.8 or higher
- Visual Studio 2019 or higher (for development)

### Steps to Run

1. Clone or download the project files
2. Open `Learnify.sln` in Visual Studio
3. Restore NuGet packages if needed
4. Build the solution (Build → Build Solution)
5. Run the application (F5 or Debug → Start Debugging)

### First Time Run

When the application runs for the first time, it automatically creates sample data including:
- 5 sample courses
- 1 sample teacher account (teacher@school.com / password: 1234)

## How to Use

### As a Student

1. Click "Register" to create a new student account
2. Fill in your details (Name, Email, Password, Education Level)
3. Login with your credentials
4. Select a difficulty level (Beginner, Intermediate, Advanced)
5. Choose a course category from the list
6. Select one or more courses from available courses
7. Choose additional materials if desired
8. Click "Enroll Now" to complete enrollment
9. View your enrollment receipt

### As a Teacher

1. Click "Teacher Login" on the main form
2. Use the sample credentials: teacher@school.com / 1234
3. View all courses in the DataGridView
4. Use buttons to:
   - Add Course: Create a new course
   - Edit Course: Modify an existing course (only your own courses)
   - Toggle Registration: Open or close registration for a course
   - View Students: See enrolled students for a course
   - Refresh: Reload the course list

## Discount Policy

| Education Level | Discount |
|-----------------|----------|
| Undergraduate Student | 40% |
| Graduate Student | 20% |
| Non Student | 0% |

## Data Storage

All data is stored in JSON files in the application directory:
- `courses.json` - Course information
- `teachers.json` - Teacher accounts
- `students.json` - Student accounts
- `enrollments.json` - Enrollment records

## Testing

The application has been tested with the following scenarios:
- Valid and invalid login attempts
- User registration validation
- Course enrollment with and without selections
- Discount calculation for different education levels
- Teacher course management (add, edit, toggle, view students)
- Access control for teacher course editing

## Future Improvements

- Add password encryption for better security
- Implement a database (SQL Server or MongoDB) instead of JSON files
- Add course search and filter functionality
- Include payment gateway integration
- Add email confirmation for successful enrollment
- Implement progress tracking for enrolled courses
- Add an admin panel for overall system management
- Include reporting features for enrollment statistics

## Author

**Rubaisha Siddiqui**

## License

This project was developed as a university assignment for educational purposes.

## Acknowledgments

- Course instructors for guidance
- .NET documentation and community resources
- Doxygen for documentation generation
