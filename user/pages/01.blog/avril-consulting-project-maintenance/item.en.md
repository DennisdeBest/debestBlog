---
title: 'Avril Consulting, Project Maintenance'
taxonomy:
    category:
        - blog
    tags:
        - avril
        - maintenance
---

Once a website is put in production and delivered to the client the fun doesn't just stop, a big part of the work is **maintenance**. 
 
Every now and again the client will want new functionality implemented or discovers a bug that needs fixing, part of my job as an intern was taking care of some of these tasks. 
 
The projects I worked on were build with *Prestashop* and this brings different challenges from building a site from the ground up. 
 
When doing maintenance you always pray for well documented code but this is hardly ever the case, it seems documentation is every programmer's least favourite activity. 
 
The first project I worked on was using *Prestashop* 1.6.1, one of the latest releases. My job was to customize the wish list module to add things like : 
* Create new wish lists straight from a dropdown when a heart icon is clicked on the product page 
* Fill in the heart icon and add new wish lists to the dropdown dynamically using Ajax 
 
This was accomplished fairly easily buy overriding the default module and adding some **jQuery**, **Ajax** and **PHP**. 
 
At this point I was feeling pretty confident when I was asked to correct some bugs on a different project again using *Prestashop* my newly found confidence was short-lived however. 
After I span up a new *Virtual Machine* it quickly became apparent that the project used version 1.5 of prestashop which is a while other animal from the previous project. 
The demands were :  
* Add some text to a contact page 
* Implement a search function to the mobile version of the website 
* Fix the geolocalization 
 
The first one was pretty straight forward but the site was not coded using **R**esponsive **W**eb **D**esing so even just adding a few lines of text completely ruined the page layout. 
After changing a few lines of CSS and changing some images the job was done in about 3 hours. 
 
Next up the implementation of the search bar in the mobile website, this turned out a lot easier than anticipated and was mostly a question of activating the module on the correct page from the back office and writing a few lines of CSS. 
 
The last one however is something dreaded by most project managers, *regression*. 
Indeed the geolocalization of the user to propose the closest store used to work and stopped all of a sudden for no apparent reason. 
After a couple of hours of research it turned out that google chrome was the culprit, starting at version 50 chrome doesn't allow geolocalization requests for non secure servers (the ones not using https). 
The only solution would be to get an SSL certificate for the server and migrating everything to https, this of course needs approval from the client as it goes beyond simple maintenance and the costs are more consequential. 
 
So that was my maintenance experience so far.