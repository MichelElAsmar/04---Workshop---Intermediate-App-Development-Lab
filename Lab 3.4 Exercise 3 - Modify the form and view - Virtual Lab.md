
Exercise - Modify the form and view
===================================

In this exercise, you modify the Machine Order form to add other columns. When you create a table in Microsoft Dataverse, it also creates a main form for that table with a few basic columns on it. In addition to the form, views are created for the table. Views are used in a model-driven app whenever a list of the table rows are displayed. You would modify the view to add more columns or change the placement. You can also create other views. For example, you might provide a view to show all machine requests that are waiting to be received.

Note

To complete the exercises, you'll need to use a few files. Download the [Student files](https://github.com/MicrosoftDocs/mslearn-developer-tools-power-platform/raw/master/in-a-day/AIAD/AppinADayStudentFiles.zip) for use in this lab.

Task: Modify the form
---------------------

To modify the form, follow these steps:

1.  Select **Solutions** and then open the **Contoso Coffee** solution.
    
2.  Select **Tables** and then open the **Machine Order** table.
    
    [![Screenshot of the device order option under tables.](media/machine-order2.png)](media/machine-order2.png#lightbox)
    
3.  Go to the **Data experiences** section and select **Forms**.
    
    [![Screenshot showing the Forms button in the Data experiences section.](media/forms.png)](media/forms.png#lightbox)
    
4.  Select the **Information Main** form and then select **Edit > Edit in new tab**.
    
    [![Screenshot showing the Edit in new tab selection.](media/edit-new-tab.png)](media/edit-new-tab.png#lightbox)
    
5.  If you're required to sign in again, do so.
    
6.  From the **Table columns** pane to the left of the screen, search for the **Approver** column and then drag it to the form.
    
7.  Place the **Approver** column above the **Machine Name** column.
    
    [![Screenshot of where the Approver column should be dragged.](media/approver2.png)](media/approver.png#lightbox)
    
8.  The new form designer lets you reposition columns. Drag the **Approver** column and place it between the **Machine Name** and **Owner** columns.
    
9.  The new form designer lets you cut and paste columns. Select the **Approver** column and then select the **Cut** button.
    
10.  Select the **Owner** column and then select **Paste**.
    
[![Screenshot of the paste icon.](media/paste3.png)](media/paste.png#lightbox)
    
    The **Approver** column is moved to the bottom.
    
[![Screenshot of the Approver column selected and moved to the bottom.](media/approver-column.png)](media/approver-column.png#lightbox)
    
11.  Select **Save and Publish**.
    
[![Screenshot of the Publish button.](media/publish2.png)](media/publish2.png#lightbox)
    
12.  Close the **Form Designer** tab.
    
13.  Select **Done**.
    

Task: Modify the view
---------------------

To modify the view, follow these steps:

1.  Select **Solutions** and then open the **Contoso Coffee** solution.
    
2.  Select **Tables** and then open the **Machine Order** table.
    
3.  Go to the **Data experiences** section and select **Views**.
    
    [![Screenshot of the Views option selected in the Data experiences section.](media/views.png)](media/views.png#lightbox)
    
4.  Open the **Active Machine Orders** option.
    
    [![Screenshot showing the Active Machine Orders view.](media/active-machine-orders.png)](media/active-machine-orders.png#lightbox)
    
5.  Select the **Approval Status** column once (you don't need to double-click).
    
    [![Screenshot of the Approval Status option.](media/approval-status.png)](media/approval-status.png#lightbox)
    
    The new column is added to the view.
    
    [![Screenshot of the new Approval Status column.](media/approval-status-column.png)](media/approval-status-column.png#lightbox)
    
6.  Select the **\+ View column** button.
    
    [![Screenshot of the View column button.](media/add-column2.png)](media/add-column.png#lightbox)
    
7.  Select **Estimated Ship Date**.
    
    [![Screenshot of the Estimated Ship Date button.](media/estimated-ship-date.png)](media/estimated-ship-date.png#lightbox)
    
8.  Add **Price** and **Status** to the view.
    
    [![Screenshot of the Price and Status columns.](media/price-status.png)](media/price-status.png#lightbox)
    
9.  Select **Save and Publish**.
    
10.  Then, select the **Back** button.
    
[![Screenshot of the Back button.](media/back-button.png)](media/back-button.png#lightbox)
