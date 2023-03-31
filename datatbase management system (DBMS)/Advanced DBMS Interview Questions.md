Advanced DBMS Interview Questions
----------------------------------
16. Explain different types of Normalization forms in a DBMS.
-------------------------------------------------------------
Following are the major normalization forms in a DBMS:

1NF: It is known as the first normal form and is the simplest type of normalization that you can implement in a database. A table to be in its first normal form should satisfy the following conditions:
Every column must have a single value and should be atomic.
Duplicate columns from the same table should be removed.
Separate tables should be created for each group of related data and each row should be identified with a unique column.

Table-1 converted to 1NF form

2NF: It is known as the second normal form. A table to be in its second normal form should satisfy the following conditions:
The table should be in its 1NF i.e. satisfy all the conditions of 1NF.
Every non-prime attribute of the table should be fully functionally dependent on the primary key i.e. every non-key attribute should be dependent on the primary key in such a way that if any key element is deleted then even the non_key element will be saved in the database.

Breaking Table-1 into 2 different tables to move it to 2NF.

3NF: It is known as the third normal form. A table to be in its third normal form should satisfy the following conditions:
The table should be in its 2NF i.e. satisfy all the conditions of 2NF.
There is no transitive functional dependency of one attribute on any attribute in the same table.

Breaking Table-1 into 3 different tables to move it to 3NF. 

BCNF: BCNF stands for Boyce-Codd Normal Form and is an advanced form of 3NF. It is also referred to as 3.5NF for the same reason. A table to be in its BCNF normal form should satisfy the following conditions:
The table should be in its 3NF i.e. satisfy all the conditions of 3NF.
For every functional dependency of any attribute A on B
(A->B), A should be the super key of the table. It simply implies that A can’t be a non-prime attribute if B is a prime attribute.

17. Explain different types of keys in a database.
--------------------------------------------------
There are mainly 7 types of keys in a database:

Candidate Key: The candidate key represents a set of properties that can uniquely identify a table. Each table may have multiple candidate keys. One key amongst all candidate keys can be chosen as a primary key. In the below example since studentId and firstName can be considered as a Candidate Key since they can uniquely identify every tuple.

Super Key: The super key defines a set of attributes that can uniquely identify a tuple. Candidate key and primary key are subsets of the super key, in other words, the super key is their superset.

Primary Key: The primary key defines a set of attributes that are used to uniquely identify every tuple. In the below example studentId and firstName are candidate keys and any one of them can be chosen as a Primary Key. In the given example studentId is chosen as the primary key for the student table.

Unique Key: The unique key is very similar to the primary key except that primary keys don’t allow NULL values in the column but unique keys allow them. So essentially unique keys are primary keys with NULL values.

Alternate Key: All the candidate keys which are not chosen as primary keys are considered as alternate Keys. In the below example, firstname and lastname are alternate keys in the database.

Foreign Key:  The foreign key defines an attribute that can only take the values present in one table common to the attribute present in another table. In the below example courseId from the Student table is a foreign key to the Course table, as both, the tables contain courseId as one of their attributes.

Composite Key:  A composite key refers to a combination of two or more columns that can uniquely identify each tuple in a table. In the below example the studentId and firstname can be grouped to uniquely identify every tuple in the table.

18. Explain the difference between a 2-tier and 3-tier architecture in a DBMS.
------------------------------------------------------------------------------
The 2-tier architecture refers to the client-server architecture in which applications at the client end directly communicate with the database at the server end without any middleware involved.
Example – Contact Management System created using MS-Access or Railway Reservation System, etc.

The 3-tier architecture contains another layer between the client and the server to provide GUI to the users and make the system much more secure and accessible. In this type of architecture, the application present on the client end interacts with an application on the server end which further communicates with the database system.

Example – Designing registration form which contains a text box, label, button or a large website on the Internet, etc.
