Create a model-driven Power Apps app for machine ordering - Virtual Lab
===========================================================================

*   lab
*   6 Units

In the first lab lab, you built a Power Apps canvas application for an organization where, every few years, the employees go through a coffee machine replacement cycle. The application allows employees to request a machine by using the app that you built. In the second lab lab, while using a custom table that you created in the Microsoft Dataverse lab, you stored that request for processing. From the requesting employee's point of view, after they’ve placed the order, the new coffee machine shows up, but a back-office process needs to happen to manage the procurement, setup of the device, and distribution of the machine to that requesting employee. In this lab, you'll build a Power Apps model-driven app that back-office staff who manage fulfilling machine requests will use. By using the model-driven app style, you can take advantage of the business process feature of model-driven apps to keep the back-office staff on track for each machine request.

Learning objectives
-------------------

In this lab, you'll:

*   Create a standalone model-driven app.
*   Customize forms for the model-driven app.
*   Use a business process flow to guide users through a process.

Prerequisites
-------------

It's recommended to complete each Lab in sequence of the virtual labs

This lab is a component of the "Power App Program" instructor-led course. A licensed user environment is obligatory for participating in these exercises. Ensure that you've completed the setup steps as previously outlined. Download the Microsoft Excel file necessary for the forthcoming exercises.

*   Introduction
    
*   Exercise - Create an app and add columns to the Machine Order table
    
*   Exercise - Add a business process flow
    
*   Exercise - Modify the form and view
    
*   Exercise - Test the application
    
*   Summary


Introduction
============

This lab has four exercises:

**Exercise 1** - Create the app in Microsoft Power Apps. In this exercise, you'll create a standalone model-driven application that will apply the same Machine Order table that you created in Microsoft Dataverse.

**Exercise 2** - Build a business process flow. In this exercise, you'll add a business process flow to the Machine Order to help guide the back-office worker through the task of managing the procurement of the requested device.

**Exercise 3** - Modify forms and views. In this exercise, you'll modify the **Machine Order** form to add other columns.

**Exercise 4** - Test the application. In this exercise, you'll test the application that you built.

About model-driven apps
-----------------------

Model-driven app design is a way to make apps by adding things like forms, charts, and dashboards to data tables. This is done using special software that doesn't require much coding. These tables are linked so that you can easily move between them and avoid duplicating data.

This kind of app is good for tasks that involve a lot of data and steps, like hiring new employees or managing sales. You need a data model in Microsoft Dataverse to make such an app.

**Table Views**: These are the lists you see when you use the app. They show which data columns are visible and which rows should appear based on certain rules.

**Table Forms**: When you click on a row in a table view, you'll see a form. You can make these forms by dragging and dropping the data columns you want to show, organized into tabs and sections.

**Business Process Flows**: These are visual guides that help you complete a task in steps. They break the task down into stages and show you what data to collect or what to do next. You can make these flows visually, and even set up different paths depending on certain conditions.