## Setup Google SQL
1. Open Google Clound console
2. Hamburger menu in the top left -> SQL -> Create Instance -> Choose instance type
3. Setup instance name and root password
4. Click the instance created
5. DATABASES - > Create database: db-books
6. USERS -> Create user: app-user
7. CONNECTIONS -> Add network (Get IP from http://whatip.me/)
8. Connect database by using db client tool 
9. Create database table
```
CREATE TABLE db_books.books (
	id INT NOT NULL AUTO_INCREMENT,
	userId varchar(100) NOT NULL,
	bookTitle varchar(255) NOT NULL,
	primary key (id)
)
ENGINE=InnoDB
DEFAULT CHARSET=utf8
COLLATE=utf8_general_ci;


ALTER TABLE db_books.books ADD author varchar(255) NULL;
ALTER TABLE db_books.books ADD image varchar(255) NULL;
ALTER TABLE db_books.books ADD dateAdded varchar(255) NULL;
ALTER TABLE db_books.books ADD dateFinished varchar(255) NULL;
ALTER TABLE db_books.books ADD summary MEDIUMTEXT NULL;
ALTER TABLE db_books.books ADD starRating int(5) NULL;
ALTER TABLE db_books.books ADD deleted TINYINT(4) NULL;

```


## Project setup
```
  npm init
  npm i -S express mysql body-parser dotenv
```