#Manual Tests for cm6213 project portfolio
##c1855378

###Walkthrough one Login/register


<p>
Once you have the server running you can then go to http://localhost:8000/admin/timesheets
this will open up the admin page with a table on it showing somethign similar to the below table.
</p>

|Agency Name|Contractor Name|Start Date|Mon  |Tue  |Wed  |Thur |Fri  |Sat  |Sun  |Status |Manager Name|
|-----------|:-------------:|:--------:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:-----:|-----------:|
|  cardiff  |   Rich Mord   | 12/12/20 |True |True |True |False|True |False|False|Pending|Jone jones  |
|  Newport  |   Dan jones   | 05/12/20 |False|False|True |True |True |True |True |Pending|stan elliot |
|    RSW    |  James lloyd  | 17/12/20 |True |True |True |False|False|True |False|Pending|lloyd evans |

<p>
Then you click on create an account the account I created is in my own name and is under the email richmord111@gmail.com password is abcd1234@ 
these wont work for you but are here as example and I left the account type as a manager this would then allow you to view the manager dash board 
when logging in. After this you can then click on my account on the righthand side of the screen and select logout. then you can click on login and 
sign in with your credentials This proves that the code from the login-form feature works as intended and the login form is comparingthe data you entered 
against the data in the database.
</p>

###WAlkthrough two emailServer

<p>
This feature I completed was working originally and I did it using a java mail server through googles settings. the way it worked was the 
contractor would submit a time sheet and then the RequestMethod.post would be triggered upon the reload of the page after the timeSheet was 
submitted, both the manager andthe contractor would get emails. One to contrator as a receipt for the timeSheet and the other to the 
manager as a notification that he has had someone submit a time sheet.

The email feature I created was improved upon by Callum Rogers, who changed some of the code so that it takes the email of the contractor 
and manager from the database and sends the email to them.

To test the email function you need to login to the admin account and create a managers account using the provided email uni202019@gmail.com 
you can make a password up of you choosing or use the also provided password for simplicity and keeping all the same abcd1234@ you must also 
remember the manager name created for when you assign him to the contractor later

Next you can create an account for the contractor using university202019@gmail.com as the email and again as above you can create your own password 
or use the one provided abcd1234@ you must select the managers name from the assign the manager drop down menu which should be the manager that you 
created first.

After this log in to the contractor account and create a time sheet and submit it. Once you have submittedhead on over to google mail and sign in 
using university202019@gmail with the password abcd1234@ all lower case and you will see in the inbox an email has been recieved by the contractor 
as receipt for his submission although this needs a little work to be  sending the actual details he entered as a reiept but the email functionality 
is their

You can then log out of the gmail account and log back in using the uni202019@gmail.com email and the password is abcd1234@ all lower case as above 
and you will also see there is an email in the inbox for the manager stating that he recieved a timesheet.
</p>

####gmail account details manager
<p>
email is uni202019@gmail.com
password is abcd1234@
</p>

####gmail account details contractor
<p>
email is university202019@gmail.com
password is abcd1234@
</p>

###Feature three timeSheetManager

<p>
first you will need to create a bunch of time sheets as above walkthrough tells you how to log in with the users details 
you created and creat 3 time sheets for the last 3 weeks.

once this is done head on over to the managers account you created in the previous walk through and log in to this.you will imediately see a table in front of 
you that looks similar to the table below
</p>

|Agency Name|Start Date|Firstname|Lastname|Mon  |Tue  |Wed  |Thur |Fri  |Sat  |Sun  |Overtime |Accept/Reject|
|-----------|:--------:|:-------:|:------:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:-------:|-----------:|
|  cardiff  | 12/12/20 | Richard |Mordecai|True |True |True |False|True |False|False|   0.0   |     Y/N    |
|  Newport  | 05/12/20 |  James  | jones  |False|False|True |True |True |True |True |   0.0   |     Y/N    |
|    RSW    | 17/12/20 | Callum  | Rogers |True |True |True |False|False|True |False|   0.0   |     Y/N    |

<p>
to the right is an acceot button and reject button accept one reject one and leave the last one their. click on the history button
you will be greeted with a table displying accepted, rejected and pending time sheets this then shows you as the tester that the querys
used for this and the code writted is doing what it should be as you will see this table

You can also use the search boxes to fully search the table for any names like contractor or agency name, you can search days worked by putting in true or false 
and over and over, which will then narrow it down more and lastly you can search the dates worked which will narrow it down to every one in the last whos worked 
the dates your looking for.
</p>

|Agency Name|Contractor Name|Start Date|Mon  |Tue  |Wed  |Thur |Fri  |Sat  |Sun  |Overtime|Status      |
|-----------|:-------------:|:--------:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:------:|-----------:|
|  cardiff  |   Rich Mord   | 06/01/20 |True |True |True |False|True |False|False|  0.0   |Accepted    |
|  Newport  |   Dan jones   | 30/12/19 |False|False|True |True |True |True |True |  0.0   |rejected    |
|    RSW    |  James lloyd  | 23/12/19 |True |True |True |False|False|True |False|  0.0   |pending     |

