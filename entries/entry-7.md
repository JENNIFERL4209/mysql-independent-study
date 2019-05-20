# Week 7 - Firebase

### Inspiration
This week I have come to the conclusion to use __Firebase__ as the database management system for my productivity app instead of MySQL. This is because there aren't sufficient resources to connect MySQL with Swift - many APIs & libraries are vague with their documentation. Therefore, I had to learn Firebase! <br>

### Learning
__What is Firebase?__ 🔥<br>
_"Firebase is a backend platform for building Web, Android, and IOS applications. It offers real-time database, different APIs, multiple authentication types and hosting platform."_ -TutorialsPoint <br>

The first thing I did to learn about Firebase is to watch [this tutorial](https://www.youtube.com/watch?v=JV9Oqyle3iE) to connect Firebase with Swift. <br> __I wanted to make sure that I can actually use Firebase in Swift before I start using Firebase.__ <br>
_Below are my notes about the tutorial._ <br>

![alt text](https://github.com/JENNIFERL4209/mysql-independent-study/blob/master/images/FirebaseNotes.png) <br>

For my app, I will be using __Real-time Database__ which allows all users to receive live updates after every change.  

So far, I have created a real-time database storing user information. <br>
![alt text](https://github.com/JENNIFERL4209/mysql-independent-study/blob/master/images/UserInformation.png) <br>

### Read and Write Data on iOS
1. ```import FirebaseDatabase```
2. ```var ref:FIRDatabaseReference? #inside class ComposeViewController: UIViewController```
3. ```ref = FIRDatabase.database().reference() #inside override func viewDidLoad()```
4. ```ref?.child("#name").childByAutoId().setValue("#textView.text")``` _write some text in the app --> update to Firebase_ 
5. Change the rules to ```true``` for __read__ and __write__
6. ```ref?.child("#name").observe(#.childAdded, with: {(#FIRDataSnapshot)``` <br>

### Firebase Tutorial for iOS Notes
1. Don't write too much nested data because every time you retrieve a data, the associated data will also be retrieved.
2. Always refer to your database. 

### Takeaways 
1. __Engineers don't die on one tree. Engineers go from one tree to the other.__ I tried my best looking for resources that can connect MySQL to Swift without cost. However, the resources were either outdated or indescriptive. Within a short amount of time, I decided to learn Firebase to accomplish my database management missions... 

### Resources
1. [Firebase Tutorial for iOS](https://www.youtube.com/playlist?list=PLMRqhzcHGw1ZRUB86rmNqG15Sr5jV-2NU)
