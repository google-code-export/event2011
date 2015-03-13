# Introduction #

To share our code, it's really easier if we have a Version Control System. That's why we are going to use SVN, a famous software versioning and a revision control system.

> ![http://upload.wikimedia.org/wikipedia/en/7/79/Subversion.png](http://upload.wikimedia.org/wikipedia/en/7/79/Subversion.png)

I will try to explain you how to use a SVN repository here.

---


|Developer(s)|Community, and developers from CollabNet, Elego, WANdisco, VisualSVN|
|:-----------|:-------------------------------------------------------------------|
|Initial release|October 20, 2000|
|Development status|Active|
|Written in|C |
|Operating system|Cross-platform|
|Type|Revision control|
|License|Apache License|
|Website|http://subversion.apache.org|


---


# Why SVN? #
> _"Apache Subversion (often abbreviated SVN) is a software versioning and a revision control system. Developers use Subversion to maintain current and historical versions of files such as source code, web pages, and documentation."_ **Wikipedia**

### But we could also use Git, Mercurial or CVS. ###

Git is more complicated (not very _user-friedly_), and runs perfectly on UNIX Systems.
There is few diferences bewteen Mercurial and SVN. Commands change, and Mercurial is better for big projects.

> |![http://gabrito.com/wp-content/uploads/2010/11/git-logo.png](http://gabrito.com/wp-content/uploads/2010/11/git-logo.png)|![http://gl2i.com/blog/beta-4.1.1/data/images/subversion_logo_hor-468x64.png](http://gl2i.com/blog/beta-4.1.1/data/images/subversion_logo_hor-468x64.png)|![http://www.aragost.com/wp-content/uploads/2010/10/mercurial-logo.png](http://www.aragost.com/wp-content/uploads/2010/10/mercurial-logo.png)|
|:------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|


---


# What is a Version Control System? #

When designing a project, it is very important to keep track of all updates made ​​by each member. This is what we call Versionning. The Versioning is also used to share code.
The code is hosted on a dedicated server.

Whenever a team member wants to code, it must have the right reflex: download the latest version of the project on his computer. He can get all the changes made ​​by other team members and can start coding on the latest version.

Once you finished coding your fonctions and that your part is functional (bug free), it should be uploaded to the SVN server. Other team members can then recover the changes and start coding on the latest project version.

> ## What happens if two people modify the project in the same time? ##

As written before, before coding, you must download the latest version of the project. Before uploading the updates, you still must download the latest version and see if any conflict appears. If no conflict is present, you can then upload your code.
So if two people are coding in the same time, the first person to upload his code will upload it without problem. The second will download the changes of the first person, look if there is conflict, and then upload its code. Simple, right?

> ## What happens if two people modify the same file? ##
No problem if you follow the method described above.


---


# SVN. How can I use it? #

You can use Windows Shell, but "there's an app for that!".

> ## Tortoise SVN ##

Tortoise SVN is an extension of Microsoft Windows Shell.
It is integrated in Windows Explorer

> ![http://upload.wikimedia.org/wikipedia/commons/thumb/4/41/TortoiseSVN.png/250px-TortoiseSVN.png](http://upload.wikimedia.org/wikipedia/commons/thumb/4/41/TortoiseSVN.png/250px-TortoiseSVN.png)

You can download TortoiseSVN <a href='http://tortoisesvn.net/downloads.html'>here.</a>

Once you have downloaded and installed it, create a new folder where you want in your computer, right click on it, and click on 'SVN Checkout'.

**URL of repository:** https://event2011.googlecode.com/svn/trunk

Then click OK.


TortoiseSVN will download all files which are on our SVN Server (provided by Google)

Congratulations, your folder is now linked with our SVN Repo!


So, make all modifications you want, add files, and then, right click on the main folder (the one you created at the beginning), and click on:

**- update:** you'll recevieve all news files and changes,

**- commit:** to put your changes online. If you commit something, don't forget to leave a comment. It will help us to know where we are.

The **first time** you commit something, you will be asked to enter a login and a password:

- login: you email adress

- password: look at it there: https://code.google.com/hosting/settings


> ### What happends if there is a conflict? ###
If there is a conflict, TortoiseSVN will tell it to you and you can't upload your code. In the file which is conflicted, you will see a change :

  * file.html:
```
<<<<<<< .mine
 your code here..
=======
 the code of s.o else here
>>>>>>> .r8
```

Then, make a change in this file (/!\ Remove the <<<<< & >>>>> /!\).

Three files have been created :

```
file.html.mine
file.html.r7
file.html.r8
```
> Remove those files and then commit angain!

> ### Oops, I have commited something which doesn't work! ###

Don't panic, right click on the main folder, **TortoiseSVN** -> **Update to Revision** -> **Show log**

Choose the revision you want, modify what you want and commit!

---


I tried to be as clear as possible, difficult in English! Thank you for correcting me and tell me any errors!