---
title: 'Avril Consulting, Project POC'
---

 So what do we (or I in this case) actually do here ? 
Well my first assignment was a Proof of concept for a client. 
 
###The problem 
 
Let me explain the use case, the client sells a lot of products by *drop shipping* from different sources, drop shipping means they don't stock any products they only resale the products provided by their partners. 
 
As you can imagine this means multiple streams of products to import from their partners and then to export to their different web shops, marketplaces, etc. 
 
Traditionally product catalogues were organised using Excel spreadsheets imported into the database, this can quickly become unmanageable when handling large volumes of products and even more so when using multiple sources for the import. 
 
Another inherent problem with this method is completeness or lack thereof, indeed it is estimated the half of the product information online is incomplete or wrong. 
 
###The solution 

![](solution.jpeg?resize=150)![](b_akeneo.png?resize=150)
 
they asked me to put together a demo that addresses this problem, a **P**roduct **I**nformation **M**anager was the awnser. 
More specifically Akeneo, an open source **PIM** based on **Symfony**. 
The first order of business was to import the excel files, therefor a connector that takes the input and *cleans* it to a format the PIM can work with needed to be created. 
Then we needed a way to map the categories of the imported products to the categories created by the end user so that it is easy to organise the products the way he wants to, some more backend development was needed aswell as an interface to set the different options for the import. The last step was the export, a special connector needed to be developed as well as another interface to manage which products to export to which shop. 
 
The clients web shops use **Prestashop** (a e-commerce framework) so a module needed to be created to import the files created by **Akeneo** as well as some configuration options. 
 
With this the POC was done, we also explored some *cron* configurations to run the import and export on a schedule instead of starting them manually. 
 
The stressful moment came when it was time to demo the POC to the client because as we all know that's when random bugs start to appear, fortunately enough everything went smoothly and the client was happy with the proposal. 
 
That was the first assignment I worked on and if you want some more technical details you can download the technical documentation I wrote up here. 