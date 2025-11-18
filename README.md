# MySQL Navigator 🚀

A small, menu-driven Windows CMD tool (batch script) that simplifies MySQL database management tasks — connect, query, export/import, backup, and manage tables and databases.

---

## Table of Contents
1. [Quick Overview](#quick-overview)
2. [Features](#features)
3. [Prerequisites](#prerequisites)
4. [Installation](#installation)
5. [Usage — Quick Start](#usage---quick-start)
6. [Menu Reference](#menu-reference)
7. [Examples and Scenarios](#examples-and-scenarios)
8. [Backups, Exports & Imports](#backups-exports--imports)
9. [Screenshots](#screenshots)
10. [Troubleshooting & Notes](#troubleshooting--notes)
11. [Contributing](#contributing)
12. [Author](#author)

---

## Quick Overview
MySQL Navigator is a single Windows batch script providing an interactive, keyboard-driven interface to common MySQL operations. Use it when you want quick, repeatable DB tasks from the command line without typing full MySQL commands every time. ⚙️

---

## Features ✨
- Secure connection prompts (server, username, hidden password)
- List and select databases
- Run arbitrary SQL queries
- Export / Import SQL files
- Backup single or all databases into timestamped .sql files
- Create, describe, insert, update, delete, truncate tables & records
- Alter table structure (add / drop / modify columns)
- Drop databases and purge database contents (with confirmation prompts)
- Helpful prompts and error messages for invalid inputs

---

## Prerequisites ✅
- Windows with Command Prompt (CMD)
- MySQL client utilities installed and available in PATH (mysql, mysqldump)
- The following folders next to the script:
  - imports/ — place .sql files to import
  - exports/ — exported SQL files will be saved here
  - backups/ — backup .sql files saved here

---

## Installation
1. Clone or download this repository into a folder.
2. Ensure `mysql` and `mysqldump` are available in your PATH (open CMD and run `mysql --version`).
3. Create the folders `imports`, `exports`, `backups` if they don't exist:
   - Example:
     ```
     mkdir imports exports backups
     ```

---

## Usage — Quick Start ▶️
1. Double-click `Mysql Navigator.bat` or run it from CMD:
2. Follow the on-screen prompts to perform operations.

---

## Menu Reference
- **Main Menu**:
  - `1`: Run Query
  - `2`: Database Operations
  - `3`: Table Operations
  - `4`: Pre-Built Operations
  - `5`: Backup Database
  - `6`: Export Database
  - `7`: Import Database
  - `8`: Delete Database
  - `9`: Delete Database Content
  - `0`: Exit

- **Database Operations** (after selecting `2` from Main Menu):
  - `1`: List Databases
  - `2`: Select Database
  - `3`: Backup Current Database
  - `4`: Backup All Databases
  - `5`: Export Current Database
  - `6`: Export Another Database
  - `7`: Import SQL File
  - `8`: Drop Current Database
  - `9`: Drop Another Database
  - `0`: Delete All Tables in Current Database
  - `-`: Delete All Tables in Another Database
  - `x`: Return to Main Menu

- **Table Operations** (after selecting `3` from Main Menu):
  - `1`: Show Tables
  - `2`: Describe Table
  - `3`: Create Table
  - `4`: Insert Records
  - `5`: Update Records
  - `6`: Delete Records
  - `7`: Truncate Table
  - `8`: Alter Table
  - `9`: Return to Main Menu

- **Pre-Built Operations** (after selecting `4` from Main Menu):
  - `1`: ALTER TABLE
  - `2`: TRUNCATE TABLE
  - `3`: CREATE TABLE
  - `4`: INSERT INTO
  - `5`: UPDATE
  - `6`: DELETE
  - `7`: DESCRIBE TABLE
  - `8`: SHOW DATABASES
  - `9`: Return to Main Menu

---

## Examples and Scenarios
- **Delete Database Content**:
  1. Choose option `9` from the main menu.
  2. Select whether to delete content from the current database or another database.
  3. Confirm the deletion to remove all tables from the selected database.

- **Backup a Database**:
  1. Choose option `5` from the main menu.
  2. Select whether to back up the current database or all databases.
  3. The backup file will be saved in the `backups` directory with a timestamp.

- **Run a Custom Query**:
  1. Choose option `1` from the main menu.
  2. Enter your SQL query when prompted.
  3. View the query results directly in the terminal.

---

## Backups, Exports & Imports
- **Backups**: Create backups of your databases using the `mysqldump` utility. Backups are saved in the `backups` folder with a timestamp.
- **Exports**: Export your database or tables to SQL files. Exports are saved in the `exports` folder.
- **Imports**: Import SQL files into your databases. Place the SQL files in the `imports` folder before starting the script.

---

## Screenshots
*Coming soon! Screenshots demonstrating the tool in action.*

---

## Troubleshooting & Notes
- **Common Issues**:
  - If you encounter `'mysql' is not recognized as an internal or external command`, ensure MySQL is installed and added to your system's PATH.
  - For permission denied errors, make sure you have the necessary privileges for the MySQL operations you're trying to perform.

- **Notes**:
  - This tool is designed for educational and personal use. Use caution when performing destructive operations like dropping databases or truncating tables.
  - Always back up your data before making significant changes.

---

## Contributing
Contributions are welcome! Please fork this repository and submit a pull request for any enhancements or bug fixes.

---

## Author
**Created by Daniel Chege**  
Feel free to modify and extend the script to suit your needs!
