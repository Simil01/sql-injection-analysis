# SQL Injection (SQLi)

SQL Injection (SQLi) is a **server-side attack** that occurs when an application includes user input directly in an SQL query without handling it safely. It mainly affects **database-driven applications**, including web applications and APIs.

### How It Works

The basic process is:

**Attacker → Application Server → Database**

The application receives user input and uses it to create an SQL query. If the input is not properly separated from SQL commands, an attacker can change how the query works. This may allow authentication bypass or unauthorized database operations.

### Impact

Depending on the application's database permissions, SQL Injection may allow an attacker to:

* Read database information
* Modify or delete records
* Bypass authentication
* Perform other unauthorized database operations

### MITRE ATT&CK

SQL Injection can be associated with **T1190 – Exploit Public-Facing Application** when a vulnerable public-facing application is exploited.

### Real-World Examples

SQL Injection was used in a 2011 attack against a Sony-related website by LulzSec. It was also used in the Albert Gonzalez campaign involving victims such as 7-Eleven.

### Prevention

The primary defense is **prepared statements with parameterized queries**, which keep SQL commands separate from user input. Other controls include input validation, least privilege, WAFs, logging, monitoring, and security testing.
