Objective

The purpose of this task was to demonstrate how a poorly secured web application can be vulnerable to SQL Injection, using DVWA (Damn Vulnerable Web Application) in a controlled laboratory environment.
The goals were to:

Understand how SQL Injection occurs

Observe the impact of insecure input handling

Learn why input validation and prepared statements are essential

Practice ethical security testing on a purpose-built vulnerable system

Tool Used: DVWA

DVWA is a deliberately insecure web application designed for learning web security. It allows students to:

Experiment with common vulnerabilities

Test attacks in a safe, legal environment

Understand how real applications should be protected

The application provides different security levels (Low/Medium/High) to show how defenses reduce risk.

Steps Performed
1. Installation and Configuration

DVWA was installed on a local server/virtual machine using a web stack (Apache, PHP, MySQL).

The database was initialized through the DVWA setup page.

The application was accessed through the browser at the local address.

2. Setting Security Level to Low

From the DVWA interface, the security level was changed to “Low.”

At this level the application performs little or no input validation, simulating a poorly coded website.

3. Performing SQL Injection Test

The SQL Injection module of DVWA was opened.

User input fields that interact with the database were tested.

By entering specially crafted input instead of normal values, the application returned unexpected database information, proving that user input was being directly included in SQL queries without sanitization.

Vulnerability Explanation
Why the Application Was Vulnerable

User input was concatenated directly into SQL statements

No filtering or escaping of special characters

No use of prepared statements or parameterized queries

This allowed an attacker to:

Modify the logic of SQL queries

Retrieve data that should be private

Bypass authentication mechanisms

Security Impact

If this were a real system, SQL Injection could lead to:

Exposure of usernames and passwords

Leakage of personal or financial data

Unauthorized login without credentials

Full compromise of the database server

This demonstrates that SQL Injection remains one of the most critical web vulnerabilities.
