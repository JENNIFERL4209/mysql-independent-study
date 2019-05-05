# Week 5 - Productivity App Database

### Inspiration
This week, I worked on building a database for my productivity app. I also learned the basic commands in managing databases and tables, and I took notes for references in the future. This database stores basic data on each user's information such as _username_, _password_, and _email_. 

### Learning
Managing Database:
1. Create a database: ```CREATE DATABASE database_name;```
2. Display a database: ```SHOW DATABASES;```
3. Select a database to work with: ```USE database_name;```
4. Remove a database: ```DROP DATABASE database_name;```

Managing Table:
1. `ALTER TABLE`: modifies existing table structure (add and drop columns, change data type, add primary key, rename table, and etc.)
    
    Add Column:
    ``` 
    ALTER TABLE table_name
    ADD COLUMN email varchar(255) NOT NULL
    AFTER password #the column before email;
    ```
    Delete Column:
    ```
    ALTER TABLE table_name
    DROP COLUMN column_name;
    ```
    Rename Table:
    ```
    ALTER TABLE table_name
    RENAME TO new_table_name;
    ```

### Examples
After I created my __app__ database, I created a __user_information__ table within the database.
```
CREATE TABLE user_information (
username varchar(255) NOT NULL,
password varchar(255) NOT NULL);
```
![alt text](https://github.com/JENNIFERL4209/mysql-independent-study/blob/master/images/DatabaseCommands.png) <br> 
Then, I can see the columns that I have created. <br>
```SHOW COLUMNS from table_name;```
<br>
![alt text](https://github.com/JENNIFERL4209/mysql-independent-study/blob/master/images/ShowColumns.png) <br>
I need to insert information into each column. <br>
```
INSERT INTO table_name
VALUES('value1','value2','value3') #must be corresponding orders of the columns
```
![alt text](https://github.com/JENNIFERL4209/mysql-independent-study/blob/master/images/InsertInfo.png)

### Takeaways 
1. __You learn by doing.__ Reading tutorials and coding along was my strategy in learning. This week, I built a database on my own along with many Google searches. I found that I enjoy this process a lot. If this solution doesn't work, then I will try another solution. I'll continue to try until I accomplish my goals. _I was super excited when I was able to finish the database for my project partner Xiurong to connect MySQL with Swift!_

### Resources
1. A lot of Google Searches... <br>
![alt text](https://github.com/JENNIFERL4209/mysql-independent-study/blob/master/images/GoogleSearch.png)