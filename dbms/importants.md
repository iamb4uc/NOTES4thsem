# Importants for Exam

### Entity Integrity
- For Entity Integrity Rules, each table has a primary key
- Primary Key cannot have NULL value  
```
<student>
```  

Student_ID | Student_Awards | Student_Awards |
---------- | -------------- | -------------- |


Above you can see our primary key ie Student_D, we cannot consider Student_Awards as the primary key since not every student would have recieved the award. 


### Referential Integrity
Referential Integrity Rule in DBMS is based on Primary and Foreign key. The rule defines that a foreign key has a matching primary key reference from a table to another table should be valid.
```
<Employee>
```
EMP_ID | EMP_NAME | DEPT_ID |
------ | -------- | ------- |


```
<Department>
```
DEPT_ID | DEPT_NAME | DEPT_ZONE |
------- | --------- | --------- |

The rule states that DEPT_ID in the Employee table has a matching valid DEPT_ID in the Department table.



### DBMS
DBMS is a collection of programs through which a user can create adn maintain a database. The DBMS is hence a general purpose software system that facilitates the process of defining, constructing and manipulating a databse from various applications.  
Defining a data base involves specifying the datatype structures for the data to be stored in a database.  
Contructing the database is the process of storing the data itself or some storage medium ie controlled by the DBMS.  

### DBA

### Data Models

### Data Abstruction
Database systems are made-up of complex data structures. To ease the user interection with database the developers hide internal details from users This process of hidding irrelevent details from users is called data abstruction.  
![diagram](img/3levelofda.png)  
- **Physical Level**: This is the lowest level of data abstruction. It describes how data is actually stored in databse. You can get the complex data structure details at this level.
- **Logical Level**: This is the middle level of 3-level data abstraction architecture. It describes what data is stored in database.
- **View Level**: Highest level of data abstraction. This level descibes the user interection with database system.

### Application of Data Base Management System
