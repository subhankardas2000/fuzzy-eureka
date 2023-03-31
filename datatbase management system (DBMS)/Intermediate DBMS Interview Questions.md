Intermediate DBMS Interview Questions
-------------------------------------
8. What is Data Warehousing?
----------------------------
The process of collecting, extracting, transforming, and loading data from multiple sources and storing them in one database is known as data warehousing. A data warehouse can be considered as a central repository where data flows from transactional systems and other relational databases and is used for data analytics. A data warehouse comprises a wide variety of an organization’s historical data that supports the decision-making process in an organization.

9. Explain different levels of data abstraction in a DBMS.
----------------------------------------------------------
The process of hiding irrelevant details from users is known as data abstraction. Data abstraction can be divided into 3 levels:

Physical Level:  it is the lowest level and is managed by DBMS. This level consists of data storage descriptions and the details of this level are typically hidden from system admins, developers, and users.

Conceptual or Logical level:  it is the level on which developers and system admins work and it determines what data is stored in the database and what is the relationship between the data points.

External or View level: it is the level that describes only part of the database and hides the details of the table schema and its physical storage from the users. The result of a query is an example of View level data abstraction.  A view is a virtual table created by selecting fields from one or more tables present in the database.

10. What is meant by an entity-relationship (E-R) model? Explain the terms Entity, Entity Type, and Entity Set in DBMS.
-----------------------------------------------------------------------------------------------------------------------
An entity-relationship model is a diagrammatic approach to a database design where real-world objects are represented as entities and relationships between them are mentioned.

Entity: An entity is defined as a real-world object having attributes that represent characteristics of that particular object. For example, a student, an employee, or a teacher represents an entity.

Entity Type: An entity type is defined as a collection of entities that have the same attributes. One or more related tables in a database represent an entity type. Entity type or attributes can be understood as a characteristic which uniquely identifies the entity.  For example, a student represents an entity that has attributes such as student_id, student_name, etc.

Entity Set: An entity set can be defined as a set of all the entities present in a specific entity type in a database. For example, a set of all the students, employees, teachers, etc. represent an entity set.

11. Explain different types of relationships amongst tables in a DBMS.
----------------------------------------------------------------------
Following are different types of relationship amongst tables in a DBMS system:

One to One Relationship:  This type of relationship is applied when a particular row in table X is linked to a singular row in table Y.

One to Many Relationship: This type of relationship is applied when a single row in table X is related to many rows in table Y.

Many to Many Relationship: This type of relationship is applied when multiple rows in table X can be linked to multiple rows in table Y.

Self Referencing Relationship: This type of relationship is applied when a particular row in table X is associated with the same table.

12. Explain the difference between intension and extension in a database.
------------------------------------------------------------------------
Following is the major difference between intension and extension in a database:

Intension: Intension or popularly known as database schema is used to define the description of the database and is specified during the design of the database and mostly remains unchanged.

Extension: Extension on the other hand is the measure of the number of tuples present in the database at any given point in time. The extension of a database is also referred to as the snapshot of the database and its value keeps changing as and when the tuples are created, updated, or destroyed in a database.

13. Explain the difference between the DELETE and TRUNCATE command in a DBMS.
-----------------------------------------------------------------------------
DELETE command: this command is needed to delete rows from a table based on the condition provided by the WHERE clause.

It deletes only the rows which are specified by the WHERE clause.
It can be rolled back if required.
It maintains a log to lock the row of the table before deleting it and hence it’s slow.
TRUNCATE command: this command is needed to remove complete data from a table in a database. It is like a DELETE command which has no WHERE clause.

It removes complete data from a table in a database.
It can't be rolled back even if required. ( truncate can be rolled back in some databases depending on their version but it can be tricky and can lead to data loss). Check this link for more details
It doesn’t maintain a log and deletes the whole table at once and hence it’s fast.

14. What is a lock. Explain the major difference between a shared lock and an exclusive lock during a transaction in a database.
--------------------------------------------------------------------------------------------------------------------------------
A database lock is a mechanism to protect a shared piece of data from getting updated by two or more database users at the same time. When a single database user or session has acquired a lock then no other database user or session can modify that data until the lock is released.

Shared Lock: A shared lock is required for reading a data item and many transactions may hold a lock on the same data item in a shared lock. Multiple transactions are allowed to read the data items in a shared lock.

Exclusive lock: An exclusive lock is a lock on any transaction that is about to perform a write operation. This type of lock doesn’t allow more than one transaction and hence prevents any inconsistency in the database. 

15. What is meant by normalization and denormalization?
-------------------------------------------------------
Normalization is a process of reducing redundancy by organizing the data into multiple tables. Normalization leads to better usage of disk spaces and makes it easier to maintain the integrity of the database.  

Denormalization is the reverse process of normalization as it combines the tables which have been normalized into a single table so that data retrieval becomes faster. JOIN operation allows us to create a denormalized form of the data by reversing the normalization.
