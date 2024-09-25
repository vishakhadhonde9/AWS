# Relational Database Service(RDS)-
- Amazon RDS is a managed database service customers can use to create and manage relational databases in the cloud without the operational burden of traditional database management.
- Amazon RDS supports most of the popular RDBMSs, ranging from commercial options to open-source options and even a specific AWS option. Supported Amazon RDS engines include the following:
    - Commercial: Oracle, SQL Server
    - Open source: MySQL, PostgreSQL, MariaDB
    - Cloud native: Aurora


# Data -
- Data is a collection of a distinct small unit of information.
- It can be used in a variety of forms like text, numbers, media, bytes, etc.

# Database-
- A database is an organized collection of data, so that it can be easily accessed and managed.
- The main purpose of the database is to operate a large amount of information by storing, retrieving, and managing data.

# DBMS-
- A database management system (DBMS) is a software system for creating and managing databases.
- A DBMS enables end users to create, protect, read, update and delete data in a database.

# Relational Database and Non-relational Database-
## Relational Database-
- A relational database organizes data into tables. Data in one table can link to data in other tables to create relationships.
- A table stores data in rows and columns. A row, often called a record, contains all information about a specific entry.
- With a relational database management system (RDBMS), you can create, update, and administer a relational database.
- Some common examples of RDBMSs include the following:
    - MySQL
    - PostgresQL
    - Oracle
    - Microsoft SQL Server
    - Amazon Aurora

## Non-relational Database-
- The non-relational database, or NoSQL database, stores data.
- However, unlike the relational database, there are no tables, rows, primary keys or foreign keys.
- Instead, the non-relational database uses a storage model optimized for specific requirements of the type of data being stored.
- Some of the more popular NoSQL databases are MongoDB, Apache Cassandra, Redis, Couchbase and Apache HBase.

# Connect RDS to EC2 Instance-
- Create Database-
- Add an inbound rule:
    - Type: MySQL/Aurora (or PostgreSQL)
    - Protocol: TCP
    - Port: 3306 (or 5432)
    - Source: The security group of your EC2 instance or the specific IP range.
      
- Launch an EC2 Instance-
- Configure Security Groups:
    - Create a security group (or modify an existing one) to allow inbound traffic on the database port (e.g., 3306, 5432).
    - Set the source to the security group of your EC2 instance or its public IP.

- Configure mysql on EC2-
    -  wget https://repo.mysql.com/mysql80-community-release-el9.rpm
    -  yum install mysql80-community-release-el9.rpm
    -  yum install mysql-community-server
    -  systemctl start mysqld
    -  systemctl status mysqld
- Connect to the RDS Instance-
    - mysql -h your-rds-endpoint -P 3306 -u your-username -p.
 
- SQL Query:
    -  create database Class;
    -  use class;
    -  INSERT INTO  mysql_students VALUES(1,'Maria Anders',750);
       INSERT INTO  mysql_students VALUES(2,'Ana Trujillo',890);
       INSERT INTO  mysql_students VALUES(3,'Antonio Moreno',400);
       INSERT INTO  mysql_students VALUES(4,'Thomas Hardy',910);
       INSERT INTO  mysql_students VALUES(5,'Christina',600);
   -  select * from mysql_students;



