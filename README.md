# ApexATM - Java ATM Simulator

ApexATM is a desktop ATM simulation developed in Java using the Swing toolkit. The project demonstrates object-oriented programming concepts through a practical ATM workflow with authentication, account operations, input validation, and transaction history.

This project was developed as part of the VITyarthi — Build Your Own Project submission.

## Overview

The application simulates the basic experience of using an ATM through a graphical user interface (GUI).

After logging in with a User ID and 4-digit PIN, the user can access the ATM dashboard and perform common account operations.

## Features

- User login with User ID and 4-digit PIN
- Balance enquiry
- Cash withdrawal
- Quick cash withdrawal
- Cash deposit
- Fund transfer
- PIN change
- Transaction history / mini statement
- Bill payment
- Input validation
- Prevention of negative transaction amounts
- Prevention of withdrawals greater than the available balance
- GUI-based interaction using Java Swing

## Functional Modules

1. **Authentication Module** — validates the User ID and PIN.
2. **Account Operations Module** — handles balance enquiry, deposits, withdrawals, transfers, quick cash, bill payments, and PIN changes.
3. **Transaction History Module** — records transaction details and displays recent transaction history.
4. **User Interface Module** — provides the login screen and ATM dashboard.

## Technologies and Tools

- **Language:** Java
- **GUI:** Java Swing
- **JDK:** JDK 8 or later
- **Version Control:** Git / GitHub
- **External Libraries:** None
- **Database:** None
- **Build Tool:** None

The project was tested with JDK 17.

## Prerequisites

Install:

- Java Development Kit (JDK) 8 or later
- Git, if cloning the repository
- A terminal / command prompt

Verify Java installation:

```bash
java -version
javac -version
```

## Installation and Setup

### 1. Clone the repository

```bash
git clone https://github.com/adityarghh/ApexATM-Project.git
cd ApexATM-Project
```

### 2. Project Structure

```text
ApexATM-Project/
├── src/
│   └── atm/
│       ├── Main.java
│       ├── model/
│       │   ├── User.java
│       │   └── Transaction.java
│       ├── service/
│       │   ├── AuthService.java
│       │   └── AccountService.java
│       └── ui/
│           ├── LoginPanel.java
│           └── DashboardPanel.java
├── statement.md
├── Report.pdf
└── README.md
```

## Running from the Terminal

The project can be compiled and executed directly without an IDE.

### 1. Create an output directory

From the project root:

```bash
mkdir bin
```

### 2. Compile

```bash
javac -d bin src/atm/model/*.java src/atm/service/*.java src/atm/ui/*.java src/atm/Main.java
```

### 3. Run

```bash
java -cp bin atm.Main
```

The ATM GUI should open after the run command.

## Test Accounts

| User ID | PIN | Starting Balance |
|---|---:|---:|
| `user123` | `1234` | `$1500.00` |
| `admin` | `9999` | `$5000.00` |

## Testing

Testing can be performed manually through the GUI after compiling and running the application.

### Authentication Tests

- Use a valid User ID and PIN and verify that the dashboard opens.
- Use an incorrect PIN and verify that login is rejected.
- Use an invalid User ID and verify that login is rejected.

### Account Operation Tests

- Check the current balance.
- Deposit a valid amount and verify the balance update.
- Withdraw a valid amount and verify the balance update.
- Try to withdraw more than the available balance.
- Try to enter a negative amount.
- Transfer a valid amount to another available user.
- Change the PIN and verify the new PIN during login.
- Test quick cash and bill payment.

### Transaction Tests

- Perform a deposit, withdrawal, or transfer.
- Open the mini statement.
- Verify the transaction type, amount, resulting balance, and timestamp.

## Architecture

The project uses a layered package structure.

### Model Layer

- `User.java` — stores user/account information and transaction history.
- `Transaction.java` — represents transaction records.

### Service Layer

- `AuthService.java` — handles authentication and user management.
- `AccountService.java` — handles deposits, withdrawals, transfers, and balance updates.

### UI Layer

- `LoginPanel.java` — login interface.
- `DashboardPanel.java` — main ATM interface.

### Main Application

- `Main.java` — starts the application and controls the main UI flow.

This separation keeps the UI, application logic, and data classes organized into separate packages.

## Data Storage

ApexATM does not use a database or external file-based storage.

User and transaction information is maintained in memory while the application is running. When the application is closed, the data resets to the initial demo-account state.

## Design Decisions

- **Java Swing:** used to create a standalone desktop GUI using Java's standard libraries.
- **Layered architecture:** separates model, service, and UI responsibilities.
- **In-memory storage:** keeps the educational simulation simple and self-contained.
- **Input validation:** prevents invalid account operations and malformed input.
- **CardLayout:** allows different application screens to be displayed within a single window.
- **Service-level validation:** keeps banking rules separate from UI event handling.

## Limitations

- Data is not persistent and is lost when the application closes.
- Demo users are predefined in the application.
- The project is an educational ATM simulation and is not intended for real banking use.
- Money values use `double`, which is acceptable for this academic simulation but is not recommended for production financial systems.

## Future Enhancements

- Database-based persistent storage
- User registration
- Secure PIN storage
- Unit tests for account operations
- Improved account and transaction management
- Receipt export
- Two-factor authentication
- Additional ATM services

## Repository Contents

- `README.md` — project overview, features, setup, execution, and testing instructions.
- `statement.md` — problem statement, scope, target users, and high-level features.
- `Report.pdf` — project report.
- `src/` — organized Java source code.

## Project Information

**Project:** ApexATM — Java ATM Simulator  
**Student:** Aditya Raj  
**Registration Number:** 25BAI10708  
**Programme:** B.Tech CSE (AI/ML), 2nd Year  
**Course:** CSE2006  

## Project Repository

GitHub: https://github.com/adityarghh/ApexATM-Project
