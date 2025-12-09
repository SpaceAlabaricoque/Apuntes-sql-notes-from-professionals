---
id: 1764057197-gettingstarted
aliases:
  - Getting_Started
tags: []
---

# Getting_Started

## Create a Database 

```sql

CREATE DATABASE mydb;

```

Return Value:

`Query OK, 1 row affected`

## Use a Database

```sql

USE mydb

```

## Create Table

```sql

CREATE TABLE mytable
(
  id             int unsigned NOT NULL auto_increment,
  username       varchar(100) NOT NULL,
  email          varchar(100) NOT NULL,
  PRIMARY KEY    (id)
);

```


## Insert a Row Into a Table

```sql

INSERT INTO mytable (username, email)
VALUES ("myuser", "myuser@example.com")

```

## Updating a Row Into a Table

```sql

UPDATE mytable SET username = "myuser WHERE id = 8"

```

## Deleting a Row Into a Table

```sql

DELETE FROM mytable WHERE username = "myuser";

```

Return Value:


| id | username | email |
| ------------- | -------------- | -------------- |
| 1 | myuser | myuser@example.com |


## Show List of Existing Database

```sql

SHOW databases;

```

Return Value:

| Database |
| -------- |
| Information_schema|
| mydb |


## Show Tables in an Existing Database

```sql

SHOW tables;

```

Return value:

| Tables_in_mydb |
| ------ |
| mytable |


## Show All the Fields of a Table

```sql

DESCRIBE databaseName.tableName;

```

If already you are using a database:

```sql

DESCRIBE databaseName.tableName;

```

| Field | Type | Null | Key | Default | Extra |
| ---- | ---- | ------ | --- | ----- | ---- |
| fieldname | fieldvaluetype | NO / YES | keytype | defaultfieldvalue | |


## Creating user 

Create a local user for you database
This can only connect in local, because of that you have the localhost in the query

```sql

CREATE USER 'user'@'localhost' IDENTIFIED BY 'some_password';

```

To create a user that connect from anywhere ==(except the local machine)==.

```sql

  CREATE USER 'user'@'%' IDENTIFIED BY 'some_password';

```

## Adding Privileges

Grant basic privileges to the user for all tables of the especified database.

```sql
  
  GRANT SELECT, INSERT UPDATE ON database. * TO 'userName'@'localhost';

```

Grant ==ALL PRIVILEGES== TO THE USER FOR ==ALL TABLES== ON ==ALL DATABASE==.

```sql

  GRANT ALL ON *.* TO 'userName'@'localhost' WITH GRANT OPTION;

```





