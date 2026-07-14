# Employee Management System

A desktop GUI application for managing employee records, built with Java Swing. Employee data is stored in flat text files (no database required).

## Install

1. Make sure you have a JDK installed (Java 8+).
2. Put all `.java` files in the same folder.
3. Compile and run:
   ```
   javac *.java
   java Main
   ```
4. On first run, the app will create `idlist.txt` and per-employee `UAP<id>.txt` files in the working directory as records are added.

## Features

- **Main Menu** — gradient-themed window with buttons for Add, Remove, Update, and View
- **Add Employee** — form to enter name, salary, address, phone, email, blood group, graduation subject, designation, and department; auto-generates a random Employee ID; validates name, salary, phone number, and email before saving
- **Remove Employee** — select an existing Employee ID from a dropdown and delete their record
- **Update Employee** — select an Employee ID, load their current info, and edit salary, address, phone, or designation
- **View List** — select an Employee ID and view their full details in a popup dialog

## Data Storage

- `idlist.txt` — running list of all active Employee IDs
- `UAP<employeeID>.txt` — one text file per employee containing their record (name, salary, address, phone, email, blood group, graduation subject, designation, department, ID)

## Validation Rules

- **Name** — no digits or special characters, cannot be empty
- **Salary** — numeric, between 5–6 digits (roughly 10,000–100,000)
- **Phone Number** — must be exactly 11 digits and start with `01`
- **Email** — must be a `@gmail.com`, `@hotmail.com`, or `@yahoo.com` address with no spaces

## Project Structure

| File | Purpose |
|---|---|
| `Main.java` | Application entry point |
| `Window.java` | Main menu panel with navigation buttons |
| `AddEmployee.java` | Add-employee form and logic |
| `RemoveEmployee.java` | Remove-employee form and logic |
| `Update.java` | Update-employee form and logic |
| `View.java` | View-employee-details form |
| `Employee.java` | Employee data model |
| `ValidationMethods.java` | Input validation logic |
| `myException.java` | Custom exception + dialog messages for invalid input |
| `idList.txt` | Stores active employee IDs (generated at runtime) |

## Requirements

- Java Development Kit (JDK) 8 or later
