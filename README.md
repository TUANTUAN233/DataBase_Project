# DataBase_Project
A database system project manage the midwife services.  

ER_model.pdf provides the ER model which designed to be implemented.  

SQL files are the implementation of model.  

GoBabbyApp.java is a JDBC program that connected to the database.  

createtbl.sql could be excuted by createtbl.sh  

droptbl.sql could be excuted by droptbl.sh  

loaddata.sql could be excuted by loaddate.sh  

GoBabbyApp functionality:
When the application starts up, it will ask the midwife to enter their "practitioner id"  

Please enter your practitioner id [E] to exit:  

If the user types E, the application will exit. 
If the practitioner id entered is not valid (i.e., does not exist in the database), the application will throw an
error message and return back to the same menu.
If the practitioner id is valid, it will prompt the midwife to enter a date for the appointments she wants to see.  

Please enter the date for appointment list [E] to exit:  

At this point, the application would list all the appointments for that date for that midwife, ordered by time.
An additional column whose value is P or B is also to be displayed to indicate whether she is the primary or
backup midwife for that pregnancy (for which the appointment is for). If there are no appointments for that
date, it would print an appropriate message and go back to asking for the date.
   
   
An example format is given below:  

1: 10:00 P Scarlett Walker WALS-5323-5534  

2: 13:30 B Jasmine Ali ALIJ-6234-7423  

3: 15:00 P Cora Pinto PINTC-7342-7233  

Enter the appointment number that you would like to work on.  

[E] to exit [D] to go back to another date :  

If the user types E, the application will exit. (Make sure it closes any active database connections, etc., before
terminating.)  

If the user types D, the application will go back to the menu where it asks for the date. If the user selects a
number, the application would give the following menu.  

For Jasmine Ali ALIJ-6234-7423
1. Review notes
2. Review tests
3. Add a note
4. Prescribe a test
5. Go back to the appointments.
Enter your choice:  


Functionality Specs  

• Review notes  

If the user chooses 1, the application will list all the notes relevant for this pregnancy in the descending
order of date time, the output should be date-time and no more than the rst 50 characters of each note(s).
An example format shown below for conceptual purposes.  

2022-02-13 10:02:45 Baby has good movements  

2022-01-10 14:22:05 Couple would prefer home birth.  

And then display the previous menu with the 5 options.    


• Review tests  

If the user chooses 2, the application will list all the tests relevant for this pregnancy (but only the tests
relevant for the mother - this is a simplication) in the descending order of date (test prescription), the
output should be date (test prescription), test type and no more than the rst 50 characters of each
result(s). An example format shown below for conceptual purposes (put square brackets or something like
that in your output display to separate from the type of test and the text for results). If a result is not
yet available, display the text PENDING in it's place.

2022-02-01 [blood iron] A bit low, recommended supplements.  

2022-01-20 [first trimester ultrasound] Baby normal growth.  

And then display the previous menu with the 5 options.    


• Add a note  

If the user chooses 3 the application will let the user type in a text (note) that is then stored into the
system.
Please type your observation:
After which it will display the previous menu with the 5 options.  

• Prescribe a test  

If the user chooses 4, the application will let the user enter the type of test that is being prescribed and
that will be recorded in the system. Again, for simplicity, we will assume that test is for the mother.
Please enter the type of test:
For simplicity, you can assume that the prescription date and sample date of the test is the date on which
the test prescription is being entered.
After which it will display the previous menu with the 5 options.  

• Go back to the appointments  

Goes back to the previous menu and displays all the appointments once again for the date that was
originally entered by the user.  




