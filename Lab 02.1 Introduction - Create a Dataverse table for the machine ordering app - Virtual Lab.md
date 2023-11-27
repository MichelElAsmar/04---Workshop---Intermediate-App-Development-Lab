Lab 02: Create a Dataverse table for the machine ordering app - Virtual Lab
=======================================================================

*   Lab
*   5 Units

Microsoft Dataverse adds data storage and modeling capabilities to Power Apps that are scalable and straightforward to provision. In this Lab, you use Microsoft Dataverse to model and store the data from the machine ordering canvas app that you built in a previous Lab. In the next Lab, you'll build a model-driven application by using the same data that will be used by the back-office staff to process machine orders. These apps that you build on Dataverse use the same technology framework (Dataverse) that Microsoft Dynamics 365 apps are built on.

Learning objectives
-------------------

In this Lab, you'll:

*   Create a custom table and add custom columns to it.
*   Use the Power Apps form control to populate the table.
*   View the table data.
*   Create a calculated column.
*   Implement a server-side business rule.
  
  
Prerequisites
-------------

It's recommended to complete each Lab in sequence of the Create a machine ordering app with Power Apps - Virtual Lab 

This lab is a component of the "Power App Program" instructor-led course. A licensed user environment is obligatory for participating in these exercises. Ensure that you've completed the setup steps as previously outlined. Download the Microsoft Excel file necessary for the forthcoming exercises.


*  Introduction
    
*  Explore Microsoft Dataverse
    
*  Add custom tables and columns
  
*  Connect the data from the canvas app
    
    

Introduction
============

This lab includes the following three exercises.

### Explore Microsoft Dataverse

In this exercise, you'll explore Microsoft Dataverse standard tables. Tables in Microsoft Dataverse are similar to tables in a database or worksheets in Microsoft Excel. You can connect tables together with relationships that model real-world interactions between the data.

### Add custom tables and columns

In this exercise, you'll create a new custom table named Machine Order, and you'll add columns that are necessary to track the machine requests. You'll also create a server-side business rule that will default the estimated ship date.

### Connect the data from the canvas app

Now that you've created the table to store machine order requests, you'll connect your Machine Ordering canvas app to this table and then add a form to submit machine approval requests.    