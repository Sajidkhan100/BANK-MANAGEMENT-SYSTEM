# Bank Management System

## Overview
The **Bank Management System** is an ATM simulation project created in Java. It allows users to interact with their bank account, perform operations like deposits, withdrawals, balance checks, PIN changes, and more. The system is designed with a graphical user interface (GUI) using Java Swing and is connected to a database using JDBC to store user data and transaction history.

---

## Features
1. **Login & Authentication**: Users can log in using a unique PIN and card number.
2. **Deposit**: Users can deposit money into their accounts.
3. **Withdraw**: Users can withdraw money from their account, with sufficient balance checks.
4. **Mini Statement**: Displays recent transactions (deposits and withdrawals) in the user's account.
5. **Balance Enquiry**: Shows the current balance in the user's account.
6. **PIN Change**: Users can change their PIN securely.
7. **Fast Cash**: Users can quickly withdraw preset amounts such as Rs 100, Rs 500, Rs 1000, etc.
8. **Exit**: Users can exit the ATM interface and return to the login screen.

---

## Classes Overview

### 1. **`FastCash.java`**
   - Provides options for quick withdrawals in preset amounts (e.g., RS 100, RS 500, RS 1000, etc.).
   - It checks the user's balance before performing the transaction.
   - After the transaction, it updates the database with the withdrawal amount and displays a success message.

### 2. **`MiniStatement.java`**
   - Displays the user's mini statement, showing recent deposits and withdrawals.
   - Retrieves transaction history from the database and displays them in a readable format.
   - It also displays the user's current balance based on their transactions.

### 3. **`BalanceEnquiry.java`**
   - Displays the user's current balance by calculating the sum of deposits and withdrawals.
   - Retrieves transaction data from the database and calculates the balance dynamically.

### 4. **`Conn.java`** (Database Connection)
   - Responsible for establishing a connection to the MySQL database.
   - Executes SQL queries to retrieve and update data related to user transactions and account details.

### 5. **`Transactions.java`**
   - Displays a menu of available transaction options (Deposit, Withdraw, Balance Enquiry, etc.).
   - Directs the user to the appropriate class based on their selection (e.g., FastCash, Deposit, Withdrawal, etc.).

### 6. **`PinChange.java`**
   - Allows users to change their PIN.
   - Verifies the user's current PIN before allowing them to set a new PIN.
   - Updates the new PIN in the database.

### 7. **`Login.java`** (Login Interface)
   - Handles the login process.
   - Users must enter their card number and PIN to access the system.
   - Verifies the login credentials against the database.

---

## Database Structure
The system uses an SQL database to store user and transaction data. Below are the key tables:

1. **`bank`**: Stores the transactions for users (withdrawals and deposits).
   - Columns: `pin`, `date`, `type` (Deposit/Withdrawal), `amount`

2. **`login`**: Stores login credentials.
   - Columns: `pin`, `cardnumber`

3. **`signupThree`**: Stores user-specific details.
   - Columns: `pin`, `cardnumber`, `accounttype`, `balance`

---

## Technologies Used
- **Java**: The main programming language for implementing the system.
- **Swing**: Used to create the graphical user interface.
- **JDBC (Java Database Connectivity)**: Used for database interaction.
- **MySQL**: Database used to store user data and transactions.

---

## Prerequisites
1. **JDK (Java Development Kit)**: Version 8 or higher.
2. **MySQL Database**: Make sure MySQL is installed and set up for your environment.
3. **IDE**: Any Java IDE (e.g., IntelliJ IDEA, Eclipse).
4. **Database Setup**: You need to create a MySQL database and run the provided SQL script to create the necessary tables.

---

## Installation

### Clone the repository
```bash
git clone https://github.com/Sajidkhan100/BankManagementSystem.git
