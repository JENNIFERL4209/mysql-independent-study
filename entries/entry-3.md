# Week 3 - MySQL and Swift Collaboration Part 1

### Inspiration
After a class discussion on my classmates' takeaways, I reflected upon my study plan and decided to _change_ my __tentative schedule__! One of the most important takeaways that stayed with me is by learning the little pieces that will help me build my project and start from there. Then, when you realize you need to learn something else, this is when you go back to your tutorial and start __LEARNING__ again. 

### Learning 
__Filtering data__: creating specific search conditions in a table to retrieve a specific result set

```IN```: determine if a specified value matches any value in a result set <br>
```BETWEEN```: boolean operator that tests if a value exists or not 
```expr [NOT] BETWEEN begin_expr AND end_expr``` <br>
  * ```expr``` specifies the test range between begin and end __and__ they must have the same __data types__
  * true: if ```expr``` is >= ```begin_expr``` __and__ is <= ```end_expr```
    * otherwise, it returns zero
  
```LIKE```: query data based on a specific pattern ```expression LIKE pattern ESCAPE escape_character```
  * _wildcard_: percentage (__%__) and underscore (_)
  * ```%```: matches any string of zero or more characters
  * ```_```: matches any single characters
  * example: 
    * ```WHERE column_name LIKE 'j%'``` will filter column that begins with 'j' ^1
    * ```WHERE column_name LIKE '%i'``` will filter column that ends with 'i' ^2
    * ```WHERE column_name LIKE '%er%'``` will filter column that includes 'er'^3
  
```ALIAS```: improve readability of the queries through column alias and table alias ^4 <br> 
  * ```column alias```: giving a description to the column name <br>
    * ```AS```: a description is followed by this keyword, but it’s optional ```AS `description` ``` <br>
    * you can use it anywhere and refer the description anywhere except ```WHERE```
	even though ```AS``` keyword is optional, I recommend writing it because it’s more understandable to people who don’t understand MySQL to know that you are referencing a column or a table to a “nickname” <br>
  * ```table alias```: giving a table a different name
	it seems unnecessary to me when I was learning about it, but I realized that two tables can have the same column name, and ```table alias``` will give a “nickname” to the table you want to query into

<!--```JOIN```: linking data from more than one table -->

### Examples
^1![alt text](https://github.com/JENNIFERL4209/mysql-independent-study/blob/master/images/j%20example.png)<br>
^1![alt text](https://github.com/JENNIFERL4209/mysql-independent-study/blob/master/images/j%20result.png)<br>
^2![alt text](https://github.com/JENNIFERL4209/mysql-independent-study/blob/master/images/i%20example.png)<br>
^2![alt text](https://github.com/JENNIFERL4209/mysql-independent-study/blob/master/images/i%20result.png)<br>
^3![alt text](https://github.com/JENNIFERL4209/mysql-independent-study/blob/master/images/er%20example.png)<br>
^3![alt text](https://github.com/JENNIFERL4209/mysql-independent-study/blob/master/images/er%20result.png)<br>
^4![alt text](https://github.com/JENNIFERL4209/mysql-independent-study/blob/master/images/alias%20example.png)<br>
^4![alt text](https://github.com/JENNIFERL4209/mysql-independent-study/blob/master/images/alias%20result.png)<br>

### Tinkering
This week I approached the OHMySQL API to see how I can connect MySQL with Swift before beginning on my project. After reading the documentation, I downloaded everything I need: MAMP and CocoaPods. However, while I was trying the given demo project, there was an expired link and I had to reach out to the author for more information before I proceed. 

### Takeaways
1. __Be curious.__ While I was consistently learning different MySQL functions, it can get boring if you're not trying things out. This week, I tinkered mostly in a sandbox to see what I can do and added some fun to it.


### Resources
1. [OHMySQL API](https://github.com/oleghnidets/OHMySQL)
2. [MySQL Tutorial](http://www.mysqltutorial.org/basic-mysql-tutorial.aspx)






