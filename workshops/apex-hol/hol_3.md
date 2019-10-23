![](images/1a.PNG)

**Oracle Application Express: Developing Database Web Applications**

**Hands-On-Labs Guide**

*Unit 3: Creating a Database Application*

This exercise includes two hands-on-labs.

**HOL 3-1 Creating a Database Application from Scratch**: In this hands-on-lab, you create a database Web application, Demo Projects. You will extend and improve this application later.

**HOL 3-2 Creating a Database Application from a Spreadsheet**: In this hands-on lab, you use a spreadsheet to create a database Web application, Budget App. You do not extend this application but will use in a later exercise.

### HOL 3-1: Creating a Database Application from Scratch

In this lab, you create the initial application using the Create Application wizard to define multiple pages. Now that you have created the underlying tables, you are ready to create a desktop application. You will be adding reports and forms for the tables you created.
Generally, when developing an application you will not know all of the pages required at the beginning. Therefore, you will only generate a select number of pages initially, and then use the wizard to add additional pages as required. However, for this exercise you will generate most of the pages required for the application up front.

1. Using the Create Application Wizard, create the Demo Projects application. Navigate to **App Builder** and then click **Create**.
   ![](images/1_1.png)

2. You want to create a new application. Click **New Application**.   
    ![](images/1_2.png)

3. For Name, enter **Demo Projects**. For Appearance, click the **Set Appearance** icon.
    ![](images/1_3.png)

4. In the Appearance dialog, perform the following steps:

    -	For Theme Style, select **Vita – Red**.  
    -	For Application Icon, click **Choose New Icon**. Click any colored circle at the top and choose an application icon. Then click **Set Application Icon**. Click **Save Changes**.
    ![](images/1_4.png)

5. Next, add Report and Form page types for the following tables:
    - DEMO_PROJ_TEAM_MEMBERS  
    - DEMO_PROJECTS  
    - DEMO_PROJ_MILESTONES  
    -  DEMO_PROJ_TASKS  
Click **Add Page**.
    ![](images/1_5.png)

6. In the Add Page dialog, click **Report**.

7. In the Add Report Page dialog, perform the following steps:
    - For Page Name, enter DEMO_PROJ_TEAM_MEMBERS.
    - For Table or View, select **DEMO_PROJ_TEAM_MEMBERS**.
    - Select the **Include Form** checkbox and click **Add Page**.
    ![](images/1_7.png)

8. Add Report and Form page type for the DEMO_PROJECTS table.  
   Click **Add Page**.  
   In the Add Page dialog, click **Report**.  

9. In the Add Report Page dialog, perform the following steps:  
    - For Page Name, enter **DEMO_PROJECTS**.  
    - For Table or View, select **DEMO_PROJECTS**.  
    - Select the **Include Form** checkbox and click **Add Page**.

10.	Add Report and Form page type for the DEMO_PROJ_MILESTONES table.  
    Click **Add Page**.  
    In the Add Page dialog, click **Report**.

11.	In the Add Report Page dialog, perform the following steps:  
    - For Page Name, enter **DEMO_PROJ_MILESTONES**.  
    - For Table or View, select **DEMO_PROJ_MILESTONES**.  
    - Select the **Include** Form checkbox and click **Add Page**.

12.	Add Report and Form page type for the DEMO_PROJ_TASKS table.  
    Click **Add Page**.  
    In the Add Page dialog, click **Report**.

13.	In the Add Report Page dialog, perform the following steps:  
    -	For Page Name, enter **DEMO_PROJ_TASKS**.  
    -	For Table or View, select **DEMO_PROJ_TASKS**.  
    -	Select the **Include Form** checkbox and click **Add Page**.

14.	Click **Check All** next to Features.
    ![](images/1_14.png)

15.	Under Settings, select Advanced Settings.  
    Enter the following advanced settings:  
    - Short Description - enter **Maintain project details**.  
    - Description - enter **This application is used to maintain project details for the team. Projects include milestones, where you can define due dates. Tasks can be defined against a milestone or directly against the project**.  
    - Under Settings, for Add "Built with APEX" to Footer, select Yes.  
    Click **Save Changes**.
    ![](images/1_15.png)

16.	Click **Create Application**. Notice the application creation progress.

17.	The Demo Projects application is now created. Click **Run Application**.
    ![](images/1_17.png)

18.	Log in using your Workspace username and password.
    ![](images/1_18.png)

19.	Your screen should look like the following:
    ![](images/1_19.png)

### HOL 3-2: Creating a Database Application from a Spreadsheet

In this lab, you use a spreadsheet to create a database application. 

1. Navigate to **App Builder** and click **Create**.
    ![](images/hol3.2//2_1.png)

2. Select **From a File**.
   ![](images/hol3.2//2_2.png)

3. Navigate to your working directory. Drag **budget.csv** and drop it in to the Load Data dialog.
    ![](images/hol3.2//2_3b.png)

4. Click **Configure**. Then, click **Columns to Load**. Verify the data types for each of the columns.  Make sure that START_DATE and END_DATE columns have DATE Data Type. Click **Close Dialog**.
    ![](images/hol3.2//2_4.png)

5. Scroll down in the Load Data dialog. Enter **Project_Budget** for Table Name and press the <tab> key. Notice that the Error Table Name is automatically populated.  
Now, click **Load Data**.
    ![](images/hol3.2//2_5.png)

6. Table PROJECT_BUDGET is created with 73 rows. Now, click **Continue to Create Application Wizard**.
    ![](images/hol3.2//2_6.png)

7. For Name, enter **Budget App**.   
   Notice that the Home, Interactive Report with Form, and Dashboard pages are created by default. 
    ![](images/hol3.2//2_7.png)

8. For Features, click **Check All**.  
   Under Settings, click **Advanced Settings**. Remove the text for Short Description and Description.   
   Click **Save Changes**.
9. Click **Create Application**.
    ![](images/hol3.2//2_9.png)

10.	Click **Run Application**.  
    Enter your Workspace Username and Password. Click **Log In**.

11.	Your application should look like the screenshot below:
    ![](images/hol3.2//2_11.png)

12.	Review the Budget App application that you just created. Click **Budget** and then click **Dashboard** to view the respective pages.
    ![](images/hol3.2//2_12a.png)
    ![](images/hol3.2//2_12b.png)
    ![](images/last.png)






