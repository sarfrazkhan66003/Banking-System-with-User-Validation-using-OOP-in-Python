# Banking-System-with-User-Validation-using-OOP-in-Python
Banking System with User Validation using OOP in Python

Description:
This project implements a simple banking system in Python using Object-Oriented Programming (OOP) principles. The system allows users to create 
and manage bank accounts with basic functionalities such as deposits, withdrawals, account information retrieval, and viewing mini statements.
User validation is also implemented to ensure secure access to account operations.

Features:
Account Selection: Choose between Saving and Current account types.
User Validation: Ensures only valid account holders can access their accounts.
Functionalities:
Withdraw: Allows withdrawals in multiples of 100, with a limit on single transactions and a penalty for more than 5 consecutive withdrawals.
Deposit: Supports unlimited deposits without restrictions.
Account Information: Displays account type and current balance.
Mini Statement: Shows the last few transactions made on the account.
Withdrawal Limit: Maximum of 1 lakh (100,000) can be withdrawn in a single transaction.
Data Storage: Uses a dictionary to store account details, eliminating the need for file input/output.


Explaination of Code

1. Class Design
Account Class:
Represents an individual bank account.
Contains methods for managing account transactions and customer details.
Stores important information like account type, balance, and transaction history.
Holds customer-specific details such as name, address, phone, aadhaar, and pan (PAN and Aadhaar are common identifiers in India).
BankingSystem Class:
Manages multiple Account objects (each representing a user's account).
Maintains a dictionary where each key is a unique account number, and the value is an Account instance.
Provides high-level methods like creating accounts, depositing, withdrawing, viewing account info, and mini-statement access.
2. Object-Oriented Concepts
Encapsulation:
The Account class encapsulates all properties and behaviors related to a bank account, keeping them separate from other parts of the system.
Abstraction:
The code provides an interface (methods) for the user to perform banking operations without needing to understand the inner workings of each method.
Data Validation:
The code ensures that only valid account numbers are processed, adding a layer of security.
3. Functionality
Account Creation with Customer Details:
When creating an account, the user provides details like name, address, phone, Aadhaar, and PAN numbers.
A random account number is generated for each new account.
The created account is stored in the users dictionary for easy retrieval.
Deposit:
Allows the user to add funds to their account.
The deposit amount is checked to ensure it’s valid (i.e., positive).
After depositing, the balance is updated, and a record of the deposit is added to the transaction history.
Withdraw:
Enables the user to withdraw funds, but only under certain conditions:
The amount must be a multiple of 100.
It must not exceed the balance or be more than 1 lakh in a single transaction.
After five consecutive withdrawals, a penalty of 50 is applied automatically.
View Account Information:
Displays both account-related and personal information for the user.
Mini Statement:
Shows the last few transactions (up to the last five) for the user, providing a quick summary of recent activity.
4. Data Storage and Security
In-Memory Storage:
The BankingSystem class stores accounts in a dictionary, which keeps the program simple but means data isn’t saved between sessions.
User Validation:
Before performing any operation, the system checks if the account number is valid, ensuring that only existing accounts are accessed.
5. User Interaction and Input
The main program demonstrates account creation, deposit, withdrawal, account information retrieval, and mini-statement viewing using user input.
Input prompts guide the user through each process, making the program interactive.
6. Sample Usage
In the main program, the user is guided through a typical interaction with the banking system:
Creating an account.
Making a deposit.
Making a withdrawal.
Viewing account information.
Viewing a mini statement.
7. Output Structure
For each action, the program provides feedback in the console:
Successful actions (like deposits and withdrawals) print the updated balance.
Errors (like insufficient balance or incorrect account number) print relevant error messages.
8. Possible Extensions
Persistent Storage:
Currently, data is stored in-memory (not saved when the program ends). This can be improved by saving account data to a file or database.
Additional Validation:
Extra validation could be added, such as checking the format of Aadhaar and PAN numbers.
Enhanced UI:
This console-based interaction could be upgraded to a graphical user interface (GUI) or a web interface.

Conclusion
The Banking System with User Validation using OOP in Python demonstrates a structured and modular approach to developing a simple banking application. By leveraging Object-Oriented Programming (OOP) principles, the project successfully encapsulates account details and operations within classes, making the code organized, reusable, and maintainable.

Key takeaways from this project include:

OOP Principles: Encapsulation, abstraction, and modularity make the codebase easier to understand and extend. The separation of Account and BankingSystem classes allows for clear distinction between individual account management and overall system operations.

User Validation and Security: Basic user validation ensures that only authorized users can access account functions, adding a layer of security to the system.

Feature Completeness: The banking system supports essential functionalities such as deposits, withdrawals with limits, account information retrieval, and mini statements. Additionally, customer details (name, address, phone, Aadhaar, PAN) enhance the realism and practical utility of the program.

Interactive and User-Friendly: The system guides users through each step, making it easy to create accounts and perform transactions, while ensuring input validity and error handling.

Scalability: This basic structure can easily be extended to add more functionalities, such as persistent data storage, improved data validation, and enhanced security.
