# 🚀 Banking Management System (Java + MySQL)

A lightweight command-line banking system built using Core Java, JDBC, and MySQL.
This project implements the fundamental operations of a banking system with secure authentication, account handling, and transaction management — fully backed by a relational database.

## 🛠️ Tech Stack

- Technology	Purpose
- Java (JDK 21)	Application logic
- MySQL	Database storage
- JDBC	Database connectivity
- MySQL Connector/J	JDBC driver
- IntelliJ / Eclipse	IDE (any works)

## 📌 Features
### 🔐 User Management

- Register new users
- Login using email & password
- Validates duplicate accounts

### 🏦 Account Operations

- Open a new bank account
- Auto-generated unique account number
- Stores full name, balance, and 4-digit PIN

### 💸 Banking Transactions

- Credit money
- Debit money with insufficient balance protection
- Transfer between accounts
- PIN validation for every transaction
- Uses SQL transactions (commit, rollback) to ensure accuracy

### 💰 Balance Inquiry

- Fetch and display current balance securely

## 📁 Project Structure
```
src/
└── BankingManagementSystem/
    ├── BankingApp.java          # Main driver program
    ├── Accounts.java            # Account creation & lookup
    ├── AccountManager.java      # Debit, credit, transfer, balance
    └── User.java                # User register and login
```

## 🗄️ Database Setup

#### Create Database
```
CREATE DATABASE banking_system;
USE banking_system;
```
#### accounts Table
```
CREATE TABLE accounts (
    account_number BIGINT PRIMARY KEY,
    full_name VARCHAR(255) NOT NULL,
    email VARCHAR(255) NOT NULL UNIQUE,
    balance DECIMAL(10,2) NOT NULL,
    security_pin CHAR(4) NOT NULL
);
```
#### user Table
```
CREATE TABLE user (
    full_name VARCHAR(255) NOT NULL,
    email VARCHAR(255) PRIMARY KEY,
    password VARCHAR(255) NOT NULL
);
```
## ▶️ How to Run

### 1️⃣ Clone the repository
```
git clone https://github.com/your-username/Banking-Management-System.git
cd Banking-Management-System
```
### 2️⃣ Add MySQL Connector/J

Download: https://dev.mysql.com/downloads/connector/j/
Add the .jar to your project:
- IntelliJ → File → Project Structure → Modules → Dependencies → + → JAR
- Eclipse → Right-click Project → Build Path → Add External JARs

### 3️⃣ Update MySQL credentials

In ```BankingApp.java```:
```
private static final String url = "jdbc:mysql://localhost:3306/banking_system";
private static final String username = "root";
private static final String password = "your_password";
```
### 4️⃣ Run

Simply run: ```BankingApp.java```

## 📬 Screenshots

<img width="920"  alt="image" src="https://github.com/user-attachments/assets/7f5eb744-e31e-4a0d-8fe4-a6d6fddd75e6" />
<img width="920" alt="image" src="https://github.com/user-attachments/assets/d911c663-cf6f-4016-b973-8b9a6207ad93" />
<img width="920"  alt="image" src="https://github.com/user-attachments/assets/8d5ac127-a018-49ec-9cb8-edf8d4c63537" />

## 📄 License

This project is licensed under the MIT License.

## 👤 Author

Moumoni Bera
