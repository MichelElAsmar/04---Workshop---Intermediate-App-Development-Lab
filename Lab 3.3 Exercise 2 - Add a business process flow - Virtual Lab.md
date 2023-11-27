
Exercise - Add a business process flow
======================================

In this exercise, you add a business process flow to the Machine Order table to help guide the back-office worker through the task of managing procurement of the requested device.

In discovery meetings with the back-office staff, you've learned that a machine request goes through the following tasks as the staff gets the requestor their machine.

*   **Machine Requested** - Currently, this task involves sending an email to back-office personnel about the machine request. In the new Power Apps system, this task involves a Machine Order row in Microsoft Dataverse.
    
*   **Place Order** - After the back-office personnel receive the request, they'll place an order with a supplier and get an order ID.
    
*   **Receive Machine** - This task occurs when the machine is received, and the back-office workers send it to the technician to be set up with the standard configuration.
    
*   **Distribute Machine** - After the machine has been set up, it needs to be sent to the employee who requested it. Additionally, the back-office worker needs to survey the employee to make sure that they're satisfied with the machine.
    

Each task represents a milestone and will become stages in the business process flow. In a more complex scenario, you'd likely compress or potentially reimagine the business process to make it more optimal than the current process that the staff performs with their existing process.

For this lab, the **Receive Machine** and **Distribute Machine** stages are marked as optional. While you'd need to create these stages for a full implementation of the scenario, to save time, you can skip them or do them as a take-home exercise.

The completed business process flow resembles the following image.

[![Screenshot of the completed business process flow.](media/business-process-flow.png)](media/business-process-flow.png#lightbox)

Note

To complete the exercises, you'll need to use a few files. Download the [App in a Day files](https://github.com/MicrosoftDocs/mslearn-developer-tools-power-platform/raw/master/in-a-day/AIAD/AppinADayStudentFiles.zip) for use in this lab.

Task: Create business process flow
----------------------------------

To create a business process flow, follow these steps:

1.  Select **Solutions** and then open the **Contoso Coffee** solution.
    
2.  Select **\+ New** and then select **Automation > Process > Business process flow**.
    
    [![Screenshot showing the create new business process flow button.](media/create-new-business-process-flow.png)](media/create-new-business-process-flow.png#lightbox)
    
3.  Enter `Machine Procurement Process` in the **Display name** field, select **Machine Order** from the **Table** dropdown menu, and then select **Create**. When you create the business process flow behind the scenes, it creates another table with the same name as the business process flow to track the progress of each business process on the row. Therefore, make sure that you choose your name carefully; for example, you wouldn't want to use the same name as your table (such as Machine Order). For this exercise, enter the name as `Machine Procurement Process`.
    
    Note
    
    After you select **OK**, a new window will be loaded with the designer. If you have pop-up blockers enabled, this window might be blocked. Additionally, the window might not immediately have focus, so you might need to manually bring it into focus.
    
[![Screenshot of the New business process flow form with the new flow name.](media/business-process-flow-details.png)](media/business-process-flow-details.png#lightbox)
    
4.  Select the **Machine Order New Stage**, change the **Display Name** to `Machine Requested`, and then select **Apply**.
    
    [![Screenshot of the Display Name changed to Machine Requested.](media/display-name.png)](media/display-name.png#lightbox)
    
5.  Select the **Details** drop down within the step.
    
    [![Screenshot of the Details button.](media/details2.png)](media/details.png#lightbox)
    
6.  Select the **Data Step**, select **Request Date** from the **Data Field** dropdown menu, and then select **Apply**. The **Step Name** field is filled in for you automatically.
    
    [![Screenshot of the Data Step form filled in and the Apply button.](media/apply.png)](media/apply.png#lightbox)
    
7.  Select **Add** and then select **Add Data Step**.
    
    [![Screenshot of the Add Data Step button.](media/add-data-step.png)](media/add-data-step.png#lightbox)
    
8.  Select the plus (**+**) icon under **Data Step 1**.
    
    [![Screenshot of the plus icon under Data Step one.](media/add.png)](media/add.png#lightbox)
    
9.  Select **Approval Status** from the **Data Field** dropdown menu and then select **Apply**.
    
10.  Add another data step, select **Price** from the **Data Field** dropdown menu, and then select **Apply**.
    
[![Screenshot of the Apply button and Price selected from the Data Field menu.](media/apply-button.png)](media/apply-button.png#lightbox)
    
11.  Select the **Components** tab.
    
 [![Screenshot of the Components tab.](media/components.png)](media/components.png#lightbox)
    
12.  Drag **Stage** to the canvas and then place it to the right of the **Machine Requested** stage.

 [![Screenshot of where the stage should be dragged to on the canvas.](media/stage.png)](media/stage.png#lightbox)
    
13.  Select the new stage, change the **Display Name** to `Place Order`, and then select **Apply**.
    
[![Screenshot of the stage, showing the Display Name changed to Place Order and the Apply button.](media/button-apply.png)](media/button-apply.png#lightbox)
    
14.  Select **Details**.
    
15.  Select the existing **Data Step**, select **Estimated Ship Date** from the **Data Field** dropdown menu, and then select **Apply**.
    
[![Screenshot of Data Step, showing Estimated Ship Date selected from the Data Field menu and the Apply button highlighted.](media/apply-highlighted.png)](media/apply-highlighted.png#lightbox)
    
16.  Select the **Components** tab, and then drag **Data Step** to the canvas and place it under the **Estimated Ship Date** step.
    
[![Screenshot of where the data step should be dragged to on the canvas.](media/data-step.png)](media/data-step.png#lightbox)
    
17.  Select **Supplier Order ID** from the **Data Field** dropdown menu, select the **Required** checkbox, and then select **Apply**. This column isn't required; however, by selecting it at this point, you'll require users to fill out the column before they can advance to the next stage. However, the column won't block saving the row if a data value hasn't populated, as it would if the column was marked as **Required** on the column definition.
    
[![Screenshot of the Required checkbox selected.](media/required.png)](media/required.png#lightbox)
    
    Note
    
    All steps from hereon, until you reach **Task: Add a branch condition**, are optional. These steps add two more stages to the business process by using the same technique that you've already learned. You can skip ahead to **Task: Add a branch condition**.
    
18.  Select the **Components** tab and then drag **Stage** to the right side of the **Place Order** stage.
    
[![Screenshot showing Stage being dragged to the right of Place Order.](media/stage-location.png)](media/stage-location.png#lightbox)
    
19.  Select the new stage, change the **Display Name** to `Receive Machine`, and then select **Apply**.
    
[![Screenshot of the Display Name changed to Receive Machine and the Apply button.](media/receive-machine-apply.png)](media/receive-machine-apply.png#lightbox)
    
20.  Select **Details**.
    
21.  Select the existing Data Step, select **Machine Received** from the **Data Field** dropdown menu, and then select **Apply**.
    
22.  Select the **Components** tab, and then drag **Data Step** to the **Receive Machine** stage and place it under the **Machine Received** step.
    
23.  Select **Machine Configured** from the **Data Field** dropdown menu and then select **Apply**.
    
[![Screenshot of Machine Configured selected from the Data Field menu and the Apply button highlighted.](media/machine-configured-apply.png)](media/machine-configured-apply.png#lightbox)
    
24.  Add another stage and name it `Distribute Machine`.
    
25.  Add two data steps: **Machine Delivered** and **Send Survey**.
    
[![Screenshot with the two data steps added to the stage.](media/data-steps.png)](media/data-steps.png#lightbox)
    

Task: Add a branch condition
----------------------------

In this task, you add a conditional branch to your business process flow. When you did the discovery, you learned that if the price was greater than $10K, then other steps would be in place to get capital approval prior to placing the order. In this task, you determine how to modify the flow that you built to accommodate this scenario.

1.  Select the **Components** tab, and then drag **Condition** and place it between **Machine Requested** and **Place Order**.
    
 [![Screenshot of where Condition should be dragged.](media/condition2.png)](media/condition.png#lightbox)
    
2.  Select the **Condition** and change the **Display Name** to `Check Price`.
    
[![Screenshot with Condition selected and the Display Name changed to Check Price.](media/check-price.png)](media/check-price.png#lightbox)
    
3.  In the **Rules** section, select **Price** from the **Field** dropdown menu, select **Is greater than** for the **Operator**, select **Value** for **Type**, enter `10,000.00` in the **Value** field, and then select **Apply**. Columns that you use in the rules on the condition must be in the prior Stages steps, which is one reason the price was entered previously.
    
[![Screenshot of the Apply button on the Condition form.](media/condition-apply.png)](media/condition-apply.png#lightbox)
    
4.  Select **Save**.
    
[![Screenshot of the Save button.](media/save-button2.png)](media/save-button.png#lightbox)
    
    A new stage is added.
    
[![Screenshot of the new stage.](media/new-stage.png)](media/new-stage.png#lightbox)
    
5.  Select the new stage, change the **Display Name** to `Capital Approval`, and then select **Apply**.
    
6.  Select **Details**.
    
[![Screenshot of the Details menu.](media/details-menu.png)](media/details-menu.png#lightbox)
    
7.  Select the existing Data Step, select **Capital Approved** from the **Data Field** dropdown menu, and then select **Apply**.
    
[![Screenshot of Capital Approved selected from the Data Field menu and the Apply button.](media/capital-approved-apply.png)](media/capital-approved-apply.png#lightbox)
    
8.  Select **Save**.
    
9.  Select **Activate**.
    
[![Screenshot of the Activate button.](media/activate2.png)](media/activate.png#lightbox)
    
10.  Confirm the activation.
    
[![Screenshot of the activate confirmation button.](media/activate-confirmation.png)](media/activate-confirmation.png#lightbox)
    
11.  Close the process editor.
