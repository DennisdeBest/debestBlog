>It's best to have your tools with you. If you don't, you're apt to find something you didn't expect and get discouraged. 
>--<cite>Stephen King</cite> 
 
Good tools are half the job, and this is just as true when you're building a house as when you are building software. 
 
So let's take a look at some of the tools of the trade. 
 
###Version Control 
 
![](git.png) 
 
VCS is very dear to every programmer, it allows you to track changes that occurred during development and revert to any "commit" (a moment where you saved the current state of your project) in a single click. If multiple people work on the same project you can also create "branches" where you take your own copy of the code to work on which you can then "merge" with the common branch once you have finished developing a specific feature or fixed a bug, this helps tremendously when working on the same project with multiple programmers as working on the same code would create a lot of conflicts and just a lot of headaches. 
The tools we use (and nearly everyone else) is GIT and the "repositories" (projects) are stored on a private gitlab server. 
 
**Gitlab** is a webpage that provides us with a nice interface to see all the commits, comments, branches, regulate access to different repositories and pretty much manage everything we need for fast, private and secure version control. 
 
##IDE's 
 
![](phpstorm.png) 
 
Integrated development environments come in many flavours but share a common ideology, provide all the necessary tools to write software in one package. Which IDE you use comes down to personal preference, habit and sometimes cost. A few IDE's for web development are :  
* **Sublime Text**, this is more then just a text editor and provides stuff like code completing, syntax colouring, file browsing ... 
* **Atom** A lightweight IDE developed by github which comes with many plugins to customize it to your specific needs 
* **Adobe dreamweaver** if you have been following along you might recognize the name from my job interview, it is a heavyweight IDE that integrates a WYSIWYG editor, FTP transfer, code completion ... so it seems like the full package but in fact it is outdated, sluggish, expensive and cumbersome. 
* **PHP Storm** By far my favourite it has all you need and more, a local history to revert back to any point in time in case you messed up your code or deleted something you shouldn't have, git integration, ftp/sftp transfer and synchronisation, plugins for more complex code completion like Symfony, Xdebug integration, I could go on for a long time on this subject but just know this is the best IDE for web development I have ever come across. 
 
## Communication 
 
![](slack_logo_wide.png) 
 
Of course everyone has an email address but since the first email was sent by Ray Tomlinson to himself in 1971 internet communication has come a long way. In the office we use **Slack** a very handy chat tool where we can set up different channels for different subjects or projects and invite the people whom maybe concerned by said project or subject to the channel. 
 
##Project management 
 
![](logo.png) 
 
In my last post I talked about the famous SCRUM board where we pin the tasks for the day, but of course these tasks must come from somewhere and that somewhere is **Redmine**. 
**Redmine** is an online project management tools that allows the project manager to create "tickets" (tasks) and assign them to the different programmers, artists, ...  
Each task can have a priority, an estimated time and some notes, the person to whom the ticket is then assigned enters the time spend on it which allows to quickly see if the estimated time was accurate for that task and for the project as a whole. 
 
##Environments 
 
![](Vagrant.png) 
 
Not to be confused with IDE's the environment depicts the landscape on which your application will run, now traditionally every developer would install a server environment like LAMP, which stands for Linux, Apache (the most common webserver running on more than 50% of the worlds servers), MySQL (Very common Database server) and PHP (popular and powerful web programming language). 
The problems with this system start when multiple people work on the same project and they don't necessarily use the same versions of the above mentioned tools which can lead to the same code running differently on different PC's or even the server to which the application or website is deployed. 
 
To overcome this problem we now use Virtual machines (a virtual computer inside the operating system) now of course these VM's need to have the same "landscape" on every PC and ideally on the server as well. 
To accomplish this we use **Vagrant** in combination with **Ansible**, this can get a bit technical so let's just say the combination of these two tools lets you create VM's consistently with the same version of installed software across everyone's device. 
 
So that's it for the main tools that we use on a day to day basis, if you have any suggestions don't hesitate to leave a comment ;). 
 
 

 