# Week 2 - Data

### Inspiration
Last week, I found three MySQL tutorials online. Although they have similar content, their pacing was different. My solution to this problem is to create a [structural study plan](https://docs.google.com/spreadsheets/d/1I51gzCNBWmqIIOoYM1kNFV3vBxlxAhPDLNFUw4u5dUw/edit?usp=sharing) for myself. It's simple and allows me to pace myself for what I should do each week.

### Learning
__Querying data:__ _requesting data information_
1. SELECT: retrieve data from a table in your database ``` SELECT column_name FROM table_name ``` <br>
  * When you want to select _multiple columns_, you follow each column_name by a __comma (,)__. ^1 <br> 
  * If you want to select _all columns_, an __asterisk (*)__ would do the magic for you. <br>
    * Now, be __careful__ of how you're using __*__ because it may return the columns that you are not going to use and may cause traffic between the server and the application. Additionally, you might expose some _sensitive_ information such as passwords to unauthorized users. 
2. SELECT DISTINCT: delete duplicated rows in a table ```SELECT DISTINCT column_name FROM table_name WHERE condition ORDER BY column_name``` <br>
  * When there is a ```NULL``` value in your column, MySQL will keep __one__ ```NULL``` value and __deletes__ the rest that also has ```NULL``` values.
    * You can set a condition in ```WHERE``` by stating ```state IS NOT NULL``` which will not return a column with ```NULL``` values.
  * ```GROUP BY``` also has the same functionality as ```DISTINCT```.
  * ```LIMIT``` stops searching after it finds the number of unique rows specified.
 
__Filtering data:__ _choosing a specific part of the data_
1. ORDER BY: sort result set by single/multiple column(s) in a(n) ascending/descending order ^3
  * ```ORDER BY column1 [ASC|DESC], column2 [ASC|DESC]```
2. WHERE: specify a specific search condition 
  * search condition only evaluates to _true, false, or unknown_.
  * ```ADD``` operator ^2
    * |         |True  |False|Null | 
      |---------|------|-----|-----|
      |__True__ |True  |False|Null |  
      |__False__|False |False|False|
      |__Null__ |Null  |False|Null |
      * zero is considered false and non-zero is true.
    * ```ADD``` is often used in ```WHERE, SELECT, UPDATE, DELETE``` and also in ```JOIN``` statements. 
    * FUN FACT: __short-circuit evaluation:__ when evaluating an expression that has  ```ADD```, if the first part of the expression is false, then MySQL _stops_ evaluating and concludes the statement as false.
  * ```OR``` operator ^4
    * |         |True  |False|Null | 
      |---------|------|-----|-----|
      |__True__ |True  |True |True |  
      |__False__|True  |False|Null |
      |__Null__ |True  |Null |Null |
    * FUN FACT: __operator precedence:__ when there is more than one logical operator, ```AND``` is _always_ evaluated before ```OR``` operator. If you want to change the order, then you can use __parentheses ()__.
  * |    Operator   |  Description     |  
    |---------------|------------------|     
    |   =           | equal to         |
    |   <> or !=    | not equal to     |
    |   <           | less than, usually with numeric and date/time data types|
    |   >           | greater than     |  
    | <= or >=      | less than or equal to __or__ greater than or equal to   |

### Examples    
[All the examples come from an employees database and in a sandbox](http://www.mysqltutorial.org/tryit/) 

^1 ![alt text](https://github.com/JENNIFERL4209/mysql-independent-study/blob/master/images/%5E1%20select.png)<br>
^1 ![alt text](https://github.com/JENNIFERL4209/mysql-independent-study/blob/master/images/%5E1%20result.png)<br>
^2 ![alt text](https://github.com/JENNIFERL4209/mysql-independent-study/blob/master/images/%5E2%20orderby.png)<br>
^2 ![alt text](https://github.com/JENNIFERL4209/mysql-independent-study/blob/master/images/%5E2%20result.png)<br>
^3 ![alt text](https://github.com/JENNIFERL4209/mysql-independent-study/blob/master/images/%5E3%20and.png)<br>
^3 ![alt text](https://github.com/JENNIFERL4209/mysql-independent-study/blob/master/images/%5E3%20result.png)<br>
^4 ![alt text](https://github.com/JENNIFERL4209/mysql-independent-study/blob/master/images/%5E4%20or.png)<br>
^4 ![alt text](https://github.com/JENNIFERL4209/mysql-independent-study/blob/master/images/%5E4%20result.png)<br>


### Takeaways
1. Creating a __tentative schedule__ for myself is important. Not only do things happen out of control, but study plans can also be. Originally, I planned on reading sections 1-5 for this week, but I caught a cold last weekend... I was feeling crappy the whole entire week until this weekend. Therefore, I shorten my plans to sections 1-4 1/2 to avoid overload. __Making myself feel better is more important, or else no learning can even be done.__
2. __Don't copy others' blog just because mine is different.__ Learning MySQL made me realize that there isn't really a lot of code-along activities. Mostly, it's about knowing the syntax and whether you can utilize it to create a database. I think I should stop putting pressure on myself if my blog entry is different than others. __It's okay to be different.__  

### Resources 
1. [MySQL Tutorial](http://www.mysqltutorial.org/basic-mysql-tutorial.aspx)