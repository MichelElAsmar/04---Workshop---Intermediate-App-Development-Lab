
lab 1 - Create the app in Power Apps
=======================================

In this lab, you create a solution to hold your customizations, create your canvas app, and complete the first screen of the app.

Note

To complete the labs, you'll need to use a few files. Download the [Student files](https://github.com/Billy-Inatco/Power-Apps-Program/raw/main/Power%20Apps%20Labs/04%20-%20Workshop%20-%20Intermediate%20App%20Development%20Lab/All%20files/Machine-Order-Data.xlsx) for use in this lab.

Task: Sign in to Power Apps web studio
--------------------------------------

Your first task is to sign in to Power Apps web studio.

1.  Go to https://make.powerapps.com
    
    [![Screenshot of the Sign in button.](media/sign-in2.png)](media/sign-in2.png#lightbox)
    
2.  Sign in with your training account.
    
3.  Before creating an app, you need to switch to the correct environment. Select the **Environment** dropdown menu in the upper-right corner of the screen to switch to the new environment. (If your environment doesn't show, try signing out and then signing in again.)
    
    [![Screenshot of the Contoso Test environment selected.](media/test-environment2.png)](media/test-environment2.png#lightbox)
    

Task: Create a new solution
---------------------------

In this task, you create a new solution and a publisher. The solution will contain and track all your work.

1.  Select **Solutions > + New solution**.
    
    [![Screenshot of the Solutions list with a red rectangle around the add New solution button.](media/new-solution.png)](media/new-solution.png#lightbox)
    
2.  Enter `Contoso Coffee` for the **Display name** and then select the **\+ New publisher** button.
    
    [![Screenshot of the create New solution dialog with a red rectangle around the add New publisher button.](media/new-publisher.png)](media/new-publisher.png#lightbox)
    
3.  Enter `Contoso` as the **Display name**, `Contoso` as the **Name**, and `contoso` for **Prefix**. Select **Save**.
    
    [![Screenshot of the create New publisher dialog.](media/new-publisher-details.png)](media/new-publisher-details.png#lightbox)
    
4.  Select the **Contoso** publisher that you created for **Publisher** and then select **Create**.
    
    [![Screenshot of the create New solution dialog.](media/new-solution-details.png)](media/new-solution-details.png#lightbox)
    
5.  You should now be in the **Contoso Coffee** solution that you just created.
    
6.  Don't navigate away from this page.
    

Task: Create a new application
------------------------------

In this task, you create a new application by following these steps:

1.  Make sure that you're in the **Contoso Coffee** solution.
    
2.  Select **\+ New** and then select **App > Canvas app**.
    
    [![Screenshot of the create new canvas application button.](media/new-canvas-application.png)](media/new-canvas-application.png#lightbox)
    
3.  Enter `Machine Ordering App` in the **App name** field, select the **Tablet** option under **Format**, and then select **Create**.
    
    [![Screenshot of the create canvas app dialog.](media/create-canvas-app-dialog.png)](media/create-canvas-app-dialog.png#lightbox)
    
4.  If prompted, select your region and then select **Get started**.
    
5.  Select **Skip** if you receive the **Welcome to Power Apps Studio** prompt.
    

Task: Rename the screen
-----------------------

In this task, you'll rename Screen1 to Main Screen.

1.  Select the screen by selecting the **Screen1** tile in the **Tree view**.
    
2.  Select the ellipsis (**...**) next to **Screen1** (or right-click **Screen1**) and then select the **Rename** option.
    
    [![Screenshot of the Rename button.](media/rename.png)](media/rename.png#lightbox)
    
3.  Change the name to **Main Screen**.
    
    [![Screenshot of the renamed app screen.](media/renamed-app.png)](media/renamed-app.png#lightbox)
    
    Note
    
    You can also rename the screen by selecting the screen name in the right pane and then selecting the edit icon, or you can double-click the edit icon.
    
    Tip
    
    It's a good practice to rename screens and controls as you create them so that they're easier to locate as you work with Power Fx formulas that reference different controls. In this lab, you'll be prompted to rename screens and some controls. For other labs, you can rename them as you want on your own. However, make sure that you rename screens as prompted in this lab because future steps might rely on specific screen names.
    

Task: Add a header containing the app name and signed-in user's name
--------------------------------------------------------------------

Follow these steps to add a header that contains the app name and the signed-in user's name

1.  With **Main Screen** selected, select the **\+ Insert** button.
    
    [![Screenshot with an arrow pointing to the insert icon.](media/insert.png)](media/insert.png#lightbox)
    
2.  Drag **Text label** from the Insert pane and then drop it on the Main Screen.
    
    [![Screenshot with an arrow pointing to where the text label should be dragged.](media/text-label.png)](media/text-label.png#lightbox)
    
3.  Select the **Tree view** tab.
    
    [![Screenshot with an arrow pointing to the tree view icon.](media/tree-view2.png)](media/tree-view2.png#lightbox)
    
4.  Rename **Label1** to **Header Label** (refer to the previous task on renaming controls).
    
    Note
    
    Make sure that you rename this label correctly so that subsequent instructions in the lab will work as expected.
    
    [![Screenshot of the renamed label.](media/renamed-label.png)](media/renamed-label.png#lightbox)
    
5.  Select **Text** from the property dropdown list and then enter `"Machine Ordering"` in the formula bar. You can also type directly in the label.
    
    [![Screenshot of the label text.](media/label-text.png)](media/label-text.png#lightbox)
    
6.  Set the **X** and **Y** values of the Header Label to `0` from the property dropdown list at the top left of the power apps studio.
    
7.  Set the **Width** of the Header Label to `1366`.
    
    [![Screenshot of the width value of the label.](media/width-value.png)](media/width-value.png#lightbox)
    
8.  Select **Color** from the property dropdown list and set the **Color** value of the Header Label to `Color.White`.
    
9.  Set the **Fill** value of the Header Label to `Color.Black`.
    
10.  Set the **Size** value of the Header Label to `18`.
    
11.  Set the **Height** value of the Header Label to `60`.
    
12.  Go to the Properties pane and select **Align center** for the **Text alignment** value.
    
  [![Screenshot showing the Text alignment value set as Align center.](media/label-text-alignment.png)](media/label-text-alignment.png#lightbox)
    

The header label should now resemble the following image.

[![Screenshot showing the header label.](media/header-label.png)](media/header-label.png#lightbox)

Tip

You can also use the formula bar or the **Advanced** tab to enter specific values, or you can use Power Fx formulas for any property on a control.

13.  Select the **\+ Insert** button and then add another **Text label** to the Main Screen. You use this label to display the signed-in user's name.
    
 [![Screenshot showing the add text label button.](media/add-text-label.png)](media/add-text-label.png#lightbox)
    
14.  Rename the label to `User Label`.
    
15.  Select the User Label, select **Align**, and then select **Align right**. (you may need to click the 3 dots (ellipses) to show the alignment options)
    
   [![Screenshot showing the label alignment.](media/label-alignment.png)](media/label-alignment.png#lightbox)
    
16.  Set the **X** value of the User Label to `1160`.
    
17.  Set the **Y** value of the User Label to `0`.
    
18.  Set the **Width** value of the User Label to `200`.
    
19.  Set the **Color** value of the User Label to `Color.Gray`.
    
20.  Set the **Text** value of the User Label to the following formula:
    
     ` "Hello, " & User().FullName ` 
    
   [![Screenshot of the formula for the label text.](media/label-formula.png)](media/label-formula.png#lightbox)
    
    Note
    
    All functions in Power Apps are case sensitive. As you start typing "User," a dropdown menu of available choices will appear. It's a good idea to pick from the autocomplete options. Additionally, help text will display in the upper part of the screen, showing the required parameters. In this case, no input parameters are required.
    
21.  Select **\+ Insert**, expand the **Media** group, and then select **Image**.
    
   [![Screenshot showing the insert image button.](media/insert-image.png)](media/insert-image.png#lightbox)
    
22.  Rename the image `Logo Image`.
    
23.  Set the **Image** value of the Logo Image to the following URL:    
`"https://images-us-prod.cms.commerce.dynamics.com/cms/api/qbvttlwqcm/imageFileData/MA20RY?ver=c4b6&m=6&q=100"`
    
   [![Screenshot of the logo image U R L.](media/image-url.png
    
24.  Set the **X** and **Y** values of the Logo Image to `0`.
    
25.  Set the **Height** value of the Logo Image to `60`.
    
26.  Set the **Width** value of the Logo Image to `200`.
    
27.  The upper part of the screen should now resemble the following image.
    
   [![Screenshot showing the header of the screen.](media/header4.png)](media/header4.png#lightbox)
    
    Note
    
    The **User()** function in Power Apps allows you to retrieve the email, full name, and picture for the currently signed-in user. App users will always be signed in with their business or school account (Microsoft Azure Active Directory (Azure AD) credentials), so this information will always be available for any Power Apps application.
    

Task: Save the application
--------------------------

In this task, you save an initial version of the app. It's a good practice to keep saving app updates at regular intervals.

1.  Check if errors have occurred in the app by selecting the **App Checker** icon.
    
    [![Screenshot of the app checker icon highlighted.](media/app-checker.png)](media/app-checker.png#lightbox)
    
2.  The App Checker pane appears, displaying errors that have occurred.
    
3.  Close the App Checker pane.
    
4.  Select **Settings**.
    
    [![Screenshot showing the Settings button.](media/settings.png)](media/settings.png#lightbox)
    
    Note
    
    **Settings** may be located within the tool bar at the top of the page, or within the drop-down after selecting the **ellipsis** (...) within the tool bar.
    
5.  Change the **Icon Background fill** value to `Black`.
    
    In the application settings page, you can:
    
    *   Change your app name.
        
    *   Customize the app icon by choosing a background color and icon.
        
    
   [![Screenshot of the application settings page.](media/application-settings.png)](media/application-settings.png#lightbox)
    
6.  Select the **Display** tab to view the available screen orientation and aspect ratio settings. For this app, you leave it at the default setting of Landscape with 16:9 aspect ratio.
    
    [![Screenshot showing the app screen size and orientation.](media/screen-size-orientation.png)](media/screen-size-orientation.png#lightbox)
    
7.  Close the **Settings**.
    
8.  Select **Save**.
    
    [![Screenshot of the Save button.](media/save5.png)](media/save5.png#lightbox)
    

Tip

In Power Apps, when you save a version of your app, the first version will be published by default and will be available to everyone whom you share the app with. Subsequent saves are only visible to the app maker in the studio. You'll need to explicitly publish it so that all app users to get the update.

### Congratulations ! this is the end of lab 1.2 you can proceed to the next one !
