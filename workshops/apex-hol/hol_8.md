![](images/1a.PNG)

**Oracle Application Express: Developing Database Web Applications**

**Hands-On-Labs Guide**

*Unit 8: Creating and Using Forms*

This exercise includes two hands-on-labs.

**HOL 8-1 Updating the Form Pages in the Demo Projects Application**: In this hands-on-lab, you update the default form pages in the Demo Projects application. 

**HOL 8-2 Creating a Form on a Table and Linking a Report**: In this hands-on lab, you create a form on the PROJECT_BUDGET table. Then, you create a classic report on the PROJECT_BUDGET table and link this report to the form. This lab utilizes the Budget App application.

### HOL 8-1 Updating the Form Pages in the Demo Projects Application

In the Demo Projects application, you create a report that allows each Team Member to see their outstanding tasks.

1. Navigate to **App Builder** and run the **Demo Projects** application.

2. In the navigation menu, click **Demo Proj Team Members**.   
Then, click the Edit icon (pencil), next to a team member's name to view the modal form page, for the person you selected. 
    ![](images/1_2.png)

3. On the Developer Toolbar at the bottom of the page, click **Edit Page 3** to jump to the modal page in Page Designer.

4. In the property editor > Page > Identification, enter **Maintain Team Member** for both Name and Title.
    ![](images/1_4.png)

5. Under Rendering, select the **Demo_Proj_Team_Member** region. In the property editor, navigate to Appearance > Template Options. Click **Use Template Defaults**.
    ![](images/1_5.png)

6. In the Template Options dialog, under Advanced, for Item Width, select **Stretch Form Fields** and click **OK**. Then, click **OK**.
    ![](images/1_6.png)
    Save your changes. Click **Save**.

7. Now, modify the default Project form page to be more visually appealing and consistent with how the Maintain Team Member page was improved. Navigate to the application runtime environment. In the navigation menu, click **Demo Projects**.

8. Click one of the Project names, to open a modal dialog. 
    ![](images/1_8.png)

9. In the runtime environment, after selecting a project, in the Developer Toolbar, click **Edit Page 5**.
    ![](images/1_9.png)  

10.	In the Property Editor:
    - Identification: Name - enter **Maintain Project**
    - Identification: Title - enter **Maintain Project**

11.	Scroll down to Navigation and for Cursor Focus, select **First item on page**. Then, click **Save**.
    ![](images/1_11.png)

12.	Modify the default Milestone form page to be more visually appealing. In the Demo Projects runtime environment, navigate to the Demo Proj Milestones page and open one of the records by clicking the edit icon (pencil).
    ![](images/1_12.png)

13.	In the Developer Toolbar, click **Edit Page 7**.

14.	In the Property Editor:
    -	Identification: Name - enter **Maintain Milestone**
    -	Identification: Title - enter **Maintain Milestone**

15.	Scroll down to Navigation and for Cursor Focus, select **First item on page**. Then, click **Save**.

16.	Modify the default Task form page to be more visually appealing. In the Demo Projects runtime environment, navigate to the Demo Proj Tasks page and open one of the records by clicking the edit icon (pencil).

17.	In the runtime environment, view a record by clicking the Edit icon (pencil) for a task.

    ![](images/1_17.png)

18.	In the Developer Toolbar, click **Edit Page 9**.

19.	In the Property Editor:
    -	Identification: Name - enter **Maintain Task**
    -	Identification: Title - enter **Maintain Task**

20.	Scroll down to Navigation and for Cursor Focus, select **First item on page**.  
    Then, click **Save**.

### HOL 8-2: Creating a Form on a Table and Linking a Report

In this lab, you first create a classic report on the PROJECT_BUDGET table. Then, you create a form on the PROJECT_BUDGET table. Finally, you link the classic report to the form.

1. Navigate to **App Builder** and in the applications report, click **Budget App**.
    ![](images/2_1.png)

2. Navigate to application home page. Now, create a Classic Report on the PROJECT_BUDGET table. Click **Create Page** and then perform the following steps:
    a) Select **Report** and click **Next**
    b) Select **Classic Report** and click **Next**
    c) Enter **Project Budget Report** for Page Name and click **Next**
    d) For Navigation, select **Create a  new navigation menu entry** and click **Next**
    e) Select **PROJECT_BUDGET** for Table / View Name and click **Create**.
    ![](images/2_2e.png)

3. The report page is created successfully. Now, create a form on the PROJECT_BUDGET table. Perform the following steps:
    a) In the page designer toolbar, click **Create** and select **Page**.
    ![](images/2_3a.png)
    b) Select **Form** and click **Next**.
    c) Enter **Project Budget Details** for Name, select **Modal Dialog** for Page Mode and click **Next**.
    d) Click **Next**.
    e) Select **PROJECT_BUDGET** for Table / View Name and click **Next**.
    f) For Primary Key Type, select **Primary Key Column(s)**, and select **ID** for Primary Key Column.
    Click **Create**.
    ![](images/2_3f.png)
    The form page is created successfully.

4. The form you just created is a dialog page and so you cannot run it directly. If you click the Save and Run Page, you see this message:  
    ![](images/2_4.png)

5. You want to navigate to the Project Budget Report page in the page designer. In the toolbar, click the Navigate to previous page arrow (down arrow).
    ![](images/2_5.png)

6. Under Rendering > Regions, select **Report 1**. In the property editor, replace the existing title with **Project Budget Report**.

7. Under Rendering, expand **Columns** and select **ID**.

8. In the property editor, select **Link** for Type. Scroll down and locate Link > Target. Click **No Link Defined**.
    ![](images/2_8.png)

9. In the Link Builder – Target dialog, select the following:
    - Target > Type: **Page in this application**
    - Target > Page: Select the form page, Project Budget Details
    - Set Items > Name: **P< n >_ID** where n is the page number of the form page
    - Set Items > Value: **#ID#**
    Click **OK**
    ![](images/2_9.png)

10.	In the property editor, navigate to Link. For Link Text, click the Quick Pick and select **apex-edit-pencil.png**. 
    ![](images/2_10.png)

11.	Click **Save**. Then, click **Save and Run Page**.

12.	The Project Budget Report page is displayed. 
    **Note**: You might have to log in to the application using username and password. Then, in the navigation menu, click Project Budget Report.
    Click the Edit icon (pencil) for any row, and you see that the form dialog page is displayed.
    ![](images/2_12.png)
    ![](images/last.png)










