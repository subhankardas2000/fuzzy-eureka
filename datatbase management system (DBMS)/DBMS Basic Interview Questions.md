DBMS Basic Interview Questions
------------------------------
1. What is DBMS and what is its utility? Explain RDBMS with examples.
--------------------------------------------------------------------
DBMS stands for Database Management System, is a set of applications or programs that enable users to create and maintain a database. DBMS provides a tool or an interface for performing various operations such as inserting, deleting, updating, etc. into a database. It is software that enables the storage of data more compactly and securely as compared to a file-based system. A DBMS system helps a user to overcome problems like data inconsistency, data redundancy, etc. in a database and makes it more convenient and organized to use it. Check this DBMS Tutorial by Scaler Topics.
Examples of popular DBMS systems are file systems, XML, Windows Registry, etc.

RDBMS stands for Relational Database Management System and was introduced in the 1970s to access and store data more efficiently than DBMS. RDBMS stores data in the form of tables as compared to DBMS which stores data as files. Storing data as rows and columns makes it easier to locate specific values in the database and makes it more efficient as compared to DBMS.
Examples of popular RDBMS systems are MySQL, Oracle DB, etc.

2. What is a Database?
----------------------
A Database is an organized, consistent, and logical collection of data that can easily be updated, accessed, and managed. Database mostly contains sets of tables or objects (anything created using create command is a database object) which consist of records and fields. A tuple or a row represents a single entry in a table. An attribute or a column represents the basic units of data storage, which contain information about a particular aspect of the table. DBMS extracts data from a database in the form of queries given by the user. 

3. Mention the issues with traditional file-based systems that make DBMS a better choice?
-----------------------------------------------------------------------------------------
The absence of indexing in a traditional file-based system leaves us with the only option of scanning the full page and hence making the access of content tedious and super slow. The other issue is redundancy and inconsistency as files have many duplicate and redundant data and changing one of them makes all of them inconsistent. Accessing data is harder in traditional file-based systems because data is unorganized in them.
Another issue is the lack of concurrency control, which leads to one operation locking the entire page, as compared to DBMS where multiple operations can work on a single file simultaneously.

Integrity check, data isolation, atomicity, security, etc. are some other issues with traditional file-based systems for which DBMSs have provided some good solutions.

4. Explain a few advantages of a DBMS.
--------------------------------------
Data Sharing: Data from a single database can be simultaneously shared by multiple users. Such sharing also enables end-users to react to changes quickly in the database environment.

Integrity constraints: The existence of such constraints allows storing of data in an organized and refined manner.

Controlling redundancy in a database: Eliminates redundancy in a database by providing a mechanism that integrates all the data in a single database.

Data Independence: This allows changing the data structure without altering the composition of any of the executing application programs.

Provides backup and recovery facility: It can be configured to automatically create the backup of the data and restore the data in the database whenever required.

Data Security: DBMS provides the necessary tools to make the storage and transfer of data more reliable and secure. Authentication (the process of giving restricted access to a user) and encryption (encrypting sensitive data such as OTP, credit card information, etc.) are some popular tools used to secure data in a DBMS.

5. Explain different languages present in DBMS.
----------------------------------------------
DDL(Data Definition Language):  It contains commands which are required to define the database.
E.g., CREATE, ALTER, DROP, TRUNCATE, RENAME, etc.

DML(Data Manipulation Language): It contains commands which are required to manipulate the data present in the database.
E.g., SELECT, UPDATE, INSERT, DELETE, etc.

DCL(Data Control Language):  It contains commands which are required to deal with the user permissions and controls of the database system.
E.g., GRANT and REVOKE.

TCL(Transaction Control Language):  It contains commands which are required to deal with the transaction of the database.
E.g., COMMIT, ROLLBACK, and SAVEPOINT.

6. What is meant by ACID properties in DBMS?
--------------------------------------------
ACID stands for Atomicity, Consistency, Isolation, and Durability in a DBMS these are those properties that ensure a safe and secure way of sharing data among multiple users.

Atomicity: This property reflects the concept of either executing the whole query or executing nothing at all, which implies that if an update occurs in a database then that update should either be reflected in the whole database or should not be reflected at all.

Consistency: This property ensures that the data remains consistent before and after a transaction in a database.

Isolation: This property ensures that each transaction is occurring independently of the others. This implies that the state of an ongoing transaction doesn’t affect the state of another ongoing transaction.

Durability: This property ensures that the data is not lost in cases of a system failure or restart and is present in the same state as it was before the system failure or restart.

7. Are NULL values in a database the same as that of blank space or zero?
No, a NULL value is very different from that of zero and blank space as it represents a value that is assigned, unknown, unavailable, or not applicable as compared to blank space which represents a character and zero represents a number.

Example: NULL value in “number_of_courses” taken by a student represents that its value is unknown whereas 0 in it means that the student hasn’t taken any courses.
