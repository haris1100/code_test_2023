Do at least ONE of the following tasks: refactor is mandatory. Write tests is optional, will be good bonus to see it. 
Please do not invest more than 2-4 hours on this.
Upload your results to a Github repo, for easier sharing and reviewing.

Thank you and good luck!



Code to refactor
=================
1) app/Http/Controllers/BookingController.php
2) app/Repository/BookingRepository.php

Code to write tests (optional)
=====================
3) App/Helpers/TeHelper.php method willExpireAt
4) App/Repository/UserRepository.php, method createOrUpdate


----------------------------

What I expect in your repo:

X. A readme with:   Your thoughts about the code. What makes it amazing code. Or what makes it ok code. Or what makes it terrible code. How would you have done it. Thoughts on formatting, structure, logic.. The more details that you can provide about the code (what's terrible about it or/and what is good about it) the easier for us to assess your coding style, mentality etc

And 

Y.  Refactor it if you feel it needs refactoring. The more love you put into it. The easier for us to asses your thoughts, code principles etc


IMPORTANT: Make two commits. First commit with original code. Second with your refactor so we can easily trace changes. 


NB: you do not need to set up the code on local and make the web app run. It will not run as its not a complete web app. This is purely to assess you thoughts about code, formatting, logic etc


===== So expected output is a GitHub link with either =====

1. Readme described above (point X above) + refactored code 
OR
2. Readme described above (point X above) + refactored core + a unit test of the code that we have sent

Thank you!

RESPONSE & ANSWERS
=================
<ol>
<li style="color: blue">
    <b> In my thoughts, code is amazing because This code is awesome, optimized and understandable completely. The dependency Injections, code reusability, single responsibility principal are used in code. </b>
    <br>There are some issues I see in this code as follows
    <ul>
    <li> The code error handling is missing, we have to use transactions and commits/rollback commands to put the code in a secure block. sometime, we encounter errors after the model operation(CRUD) and the whole code get compromised, we have to manually delete the entry from table. This is a bad practice of doing code. I see there are some functions with more than 100-150 lines of codes. what if we encounter error on line 99 of 100? then we will have entries or updation in database. insted of manually reversing the code, we should use <b>"Begin Transactions", "Commits" , "Rollbacks"</b> scenarios. </li>
    <li>Comments and Descriptions is missing on functions and logic. </li>
    <li>Missing Response statuses (Missing Proper Error Handling of response too), like HTTP request must have response code with the response for exmp, 200 for successfull response ,404 for not found, 403 for forbidden etc </li>
    <li> Somewhere Array conventions are different, like somewhere array is declared as array() and somewhere like [] </li>
    <li> Use of unnecessary if/else conditions which can be replaced by ternery operators.  </li>
    <li> I spent almost 4 hours on code, as you know i could't execute the code due to missing files, so after reading many functions (can't say all function), I find this code ok.   </li>
    </ul>
</li>
<li>
I have refectored the code to some extent, like integrated error handling samples, removed extra code 
</li>
<li>
There was logical isses in TeHelper class function, which i have fixed.
</li>
</ol> 