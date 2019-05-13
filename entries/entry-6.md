# Week 6 - Data Types + Messenger Database 

### Inspiration
Last week, I completed a user information database storing user's username, password, and email. After I received some feedbacks about my database, I realized that I should __encrypt the password column__ to prevent personal information from leaking. My main goal for this week is to __create a messenger database__ for my Productivity App.

### Learning
1. Encrypting Passwords In My Previous Database 
    * __Search "encrypt MySQL columns"__
      * _Read [Stack Overflow](https://stackoverflow.com/questions/4275882/how-to-encrypt-a-specific-column-in-a-mysql-table)_.
        * The solution _kind of_ resolves my problem, but because I have to connect MySQL with my partner Xiurong, I don't want to do this step before she successfully connects MySQL with Swift. After encrypting, Xiurong would also need to write Swift to decrypt the passwords, or I can do it :)
      * _Find which [encryption function](https://dev.mysql.com/doc/refman/8.0/en/encryption-functions.html) I want to use_.
        * I have figured that I would use ```DES_ENCRYPT()	``` to encrypt the password strings. However, because I originally set up the password column as ```varchar``` - plain text - I would need to change the data type to binary data types.<br> __Since I mentioned data types here, I will share my knowledge about MySQL data types with you :)__
2. Data Types
    * Learning different data types leads to a better "design" of a database. 
      * i.e. A budgeting database is different than an employee database. For budgeting, you may want some columns to be _only_ numeric for dollar amounts. While for employee, you can use string and numeric _based on_ employee information. 
      * Therefore, it is important to learn about data types __and__ use them correctly. 
    * [alt text!](https://github.com/JENNIFERL4209/mysql-independent-study/blob/master/images/DataTypes.png)
    * Above is a list of MySQL data types. I usually use __VARCHAR__ for strings because it's more common than __CHAR__, __TINYTEXT__, and __TEXT__ in many examples.
    * For my messenger database, I am considering an ID column for each user, and I am thinking of using __numeric__ data types because I think it's easier to keep track of user with numbers. 

3. Messenger Database
    * I used [this](https://stackoverflow.com/questions/40370069/mysql-realtime-messaging) as a reference and guide.
    * [alt-text!](https://github.com/JENNIFERL4209/mysql-independent-study/blob/master/images/Message.png)
    * Let's explain!


### Examples

### Takeaways 
1. __Prioritize!__ While I spent the majority of the week focusing on my AP exams, I also spent a lot of time discussing with Xiurong on connecting MySQL with Swift. The _connector_ must be written in Swift code, so I tried my best to help her with this process. In the past weeks, I have found an API that I wanted to test, but it didn't really work out because I don't know Swift. __No worries, we scheduled a time with Xiurong's coworker to help us and see if we can connect them, finally!__
2. __Have Fun!__ At this point, I start to lose motivation and confidence that we cannout build a MVP (Minimum Viable Product). As I am wrapping up my MySQL missions for the app, I want to have fun finishing it! __I guess I need to save some energy to learn some Swift!__


### Resources
As stated above as __"hyper"__ links!