
# E-BankSim

This project is a simple **E-BankSim** implemented in **C++** that simulates a banking system for managing clients and users, including authentication, permissions, and transactions.

## Database Concept

The project uses text files as databases to store information:

* **Clients.txt**: Stores client records.
* **Users.txt**: Stores user records with login credentials and permissions.

### Client Record Fields

Each client record contains:

* Account Number
* Pin Code
* Name
* Phone
* Account Balance

Records are stored with a custom separator: `#//#`.

### User Record Fields

Each user record contains:

* Username
* Password
* Permissions (integer representing access rights)

Records are stored with a custom separator: `#//#`.

---

## Features

### Authentication

* **User Login**: Requires username and password.
* Denies access if credentials are incorrect.
* Tracks `CurrentUser` and their permissions.

### CRUD Operations

**Clients:**

* Add new clients
* Update client info
* Delete clients
* Find clients by Account Number
* Display all clients in a table-like format

**Users:**

* Add new users
* Update user info
* Delete users (Admin protected)
* Find users by username
* Display all users in a table-like format

### Transactions

* Deposit money
* Withdraw money
* Show total balances of all clients

### Permissions System

* Each user can have specific permissions to perform actions:

  * List clients
  * Add new client
  * Delete client
  * Update client info
  * Find client
  * Perform transactions
  * Manage users
* **Admin** users have full access.

---

## Menus

The project uses a **command-line interface (CLI)** with the following menus:

### Main Menu

1. Show Client List
2. Add New Client
3. Delete Client
4. Update Client Info
5. Find Client
6. Transactions
7. Manage Users
8. Logout

### Transactions Menu

1. Deposit
2. Withdraw
3. Total Balances
4. Main Menu

### Manage Users Menu

1. List Users
2. Add New User
3. Delete User
4. Update User
5. Find User
6. Main Menu

---

## How It Works

1. User logs in with username and password.
2. User’s permissions are loaded and determine access to menu options.
3. Client and user data are loaded from text files into memory (vectors).
4. Operations are performed on in-memory data.
5. Changes are saved back to text files to maintain persistence.

---

## Learning Goals

* Simulate a database using text files
* Learn file handling with `fstream` in C++
* Practice CRUD operations in a CLI project
* Implement user authentication and permission-based access control
* Understand data persistence without a real database

---

## Project Structure

* `E-BankSim.cpp` → Source code
* `Clients.txt` → Database file storing client records
* `Users.txt` → Database file storing user records
* `README.md` → Project description
