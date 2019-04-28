# Week 4 - CRUD + Transaction

### Inspiration
This week, I set my foot on __CRUD__, the acronym that every engineer will encounter at some point. I also tried creating a database in my terminal. Creating the database was a piece of cake, but getting MySQL to work in my terminal took me __forever__! Thank you, YouTube, for your _help_!

### Learning
__CRUD - Create, Read, Update, Delete__ <br>
  * ```INSERT```: insert one or more rows into table
```
INSERT INTO table(c1,c2,...) #table name 
VALUES(v1,v2,...) #number of columns and the number of values should be the same
``` 
  * ```UPDATE```: update data 
```
UPDATE table_name
SET #specifies which column to modify and the new values
    column_name1 = expr1,
    column_name2 = expr2,
    ...
[WHERE condition]; #optional clause, if omit, will update all rows in the table
```

  * ```DELETE```: delete data
 ```
DELETE FROM table_name
WHERE condition; #optional but important
 ```
  * ```REPLACE```: insert or update data

    * if the new row does not exist, then ```replace``` will insert a new row
    * if the new row already exists, then ```replace``` deletes the old row first and then inserts the new row
  * ```PRIMARY KEY``` or ```UNIQUE KEY```: determine whether the new row already exists
```
REPLACE INTO table_name(column_list)
VALUES(value_list);
```
__Transaction__ - execution operations to ensure database never contains partial operations (when one operation/function is not performed correctly)

_We're on a rescue mission!_

  * to begin a rescue, ```START TRANSACTION```
  * to commit current transaction and make the changes permanent, ```COMMIT```
  * to rollback the current transaction and cancel the changes, ```ROLLBACK```
  * to disable or enable the auto-commit mode for the current transaction, ```SET autocommit```
    * by default, MySQL automatically commits changes, to force MySQL not to:
      * ```SET autocommit = 0;``` or ```SET autocommit = OFF```
    * to enable, ```SET autocommit = 1;``` or ```SET autocommit = ON;```

### Examples
Going back to week 1, there was no problem starting, stopping, or restarting MySQL on my terminal. However, I was not writing my code in the terminal as I wrote them in a sandbox. Because of spring break, I was able to have _some spare time_ trying to figure out how to create my own database in the terminal. After following a guide online, I encountered this obstacle. <br>
![alt text](https://github.com/JENNIFERL4209/mysql-independent-study/blob/master/images/Week4_Failure.png) <br>
No, I can't just sit in front of my laptop and give up. Nobody will help me, and I need to resolve this problem on my own. I started googling why this problem occurs and how I can fix it. After trying different solutions, none of it worked. <br>
Then, I realized that the occurrence of this problem is because I cannot start the MySQL server correctly. I searched how to start the server, and a video did the magic for me. YAY! <br>
![alt text](https://github.com/JENNIFERL4209/mysql-independent-study/blob/master/images/Week4_success.png) <br>

### Takeaways 
1. __A successful engineer tries his/her best to resolve problems.__ The beauty of problems is that we can fix them. When I encountered my obstacle, I didn't want to face it because it's annoying! But it's all about problem-solving. Learning and trying to solve the problem defines success. 

### Resources
1. [YouTube Video](https://www.youtube.com/watch?v=ryvNDIX3gQA)
2. [MySQL Tutorial](http://www.mysqltutorial.org/basic-mysql-tutorial.aspx)