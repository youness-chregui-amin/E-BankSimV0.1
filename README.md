# **E-BankSim v0.1**

**E-BankSim** is a C++ console application that simulates a simple electronic banking system. It manages client information, handles transactions, and now includes **user authentication and permissions management**, bringing it closer to a real-world banking simulation.

---

## **Table of Contents**

1. [Features](#features)
2. [Login Information](#login-information)
3. [Database Structure](#database-structure)
4. [How It Works](#how-it-works)
5. [Project Structure](#project-structure)
6. [Learning Goals](#learning-goals)
7. [Changes from Previous Version](#changes-from-previous-version)

---

## **Features**

### **Client Management (CRUD)**

* Add new clients
* Update client information
* Delete clients
* Search clients by Account Number

### **Transactions**

* Deposit money
* Withdraw money
* Display total balances of all clients

### **User Management**

* Add, update, delete, and search users
* Assign permissions (Full Access / Limited Access)
* Secure login system

### **Command-Line Interface (CLI)**

* User-friendly text-based menus
* Organized navigation:

  * **Main Menu**
  * **Transactions Menu**
  * **User Management Menu**

---

## **Login Information**

**Default Admin Credentials:**

* **Username:** `admin`
* **Password:** `1234`

> Admin has full access to all functionalities: client management, transactions, and user management.

---

## **Database Structure**

**Clients.txt** – Stores client data:

| Field           | Description       |
| --------------- | ----------------- |
| Account Number  | Unique identifier |
| Pin Code        | Client PIN        |
| Name            | Client name       |
| Phone           | Contact number    |
| Account Balance | Current balance   |

**Users.txt** – Stores user data:

| Field       | Description                   |
| ----------- | ----------------------------- |
| Username    | User login name               |
| Password    | User password                 |
| Permissions | Access level (Full / Limited) |

> All records are separated using a custom delimiter: `#//#`.

---

## **How It Works**

1. The application loads data from `Clients.txt` and `Users.txt` into memory (vectors).
2. Users perform operations on in-memory data.
3. Changes are saved back to the text files immediately.
4. Users navigate via structured CLI menus:

**Main Menu**

* Show Client List
* Add New Client
* Delete Client
* Update Client Info
* Find Client
* Transactions
* Manage Users
* Logout

**Transactions Menu**

* Deposit
* Withdraw
* Show Total Balances
* Back to Main Menu

**User Management Menu**

* List Users
* Add New User
* Delete User
* Update User
* Find User
* Back to Main Menu

---

## **Project Structure**

```
E-BankSimV0.1.cpp      → Main source code
Clients.txt        → Client database
Users.txt          → User database
README.md          → Project documentation
```

---

## **Learning Goals**

* Simulate a database using text files
* Practice file handling in C++ with `fstream`
* Implement CRUD operations in a CLI project
* Understand data persistence without a real database
* Learn basic user authentication and permissions handling

---

## **Changes from Previous Version**

| Aspect              | Previous Version                 | v0.1 Professional Version                        |
| ------------------- | -------------------------------- | ------------------------------------------------ |
| User Authentication | Not included                     | Added login system with username/password        |
| User Management     | Not included                     | Full CRUD with permissions                       |
| Database Files      | Only Clients.txt                 | Clients.txt + Users.txt                          |
| Menu Structure      | Simple Main & Transactions menus | Main Menu + Transactions + User Management menus |
| Security            | None                             | Permission-based access control                  |
| CLI Experience      | Basic                            | Structured, user-friendly                        |
| Documentation       | Minimal                          | Detailed, professional, includes tables & flow   |
