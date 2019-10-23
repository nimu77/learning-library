![](images/1a.PNG)

**Oracle Application Express: Developing Database Web Applications**

**Hands-On-Labs Guide**

*Unit 10: Adding Computations, Processes, and Validations*

This exercise includes four hands-on-labs.

HOL 10-1 uses the Demo Projects application.

HOL 10-2, HOL 10-3, and HOL 10-4 use the Budget App application.

**HOL 10-1 Implementing Validations on the Maintain Project Page**: In this lab, you create and use validations on the Maintain Project page. 

**HOL 10-2 Creating and Using a Computation**: In this lab, you create a computation that changes the value of a field entered using the form to uppercase after the page is submitted

**HOL 10-3 Creating and Using a Process**: This lab covers creating an After Submit process on the Project Budget form page

**HOL 10-4 Creating and Using Validations**: In this hands-on lab, you create a not null validation and a validation to ensure that the item is numeric.

### HOL 10-1: Implementing Validations on the Maintain Project Page

In this lab, you add validations to the Maintain Projects page so that when a user changes the status to Completed, they add the Completed Date and that it is not forward-dated.

1.	Navigate to **App Builder** and run the **Demo Projects** application.

    a)	In the navigation menu, click **Demo Projects**. In the Developer Toolbar, click **Edit Page 4**.
    b)	Under Rendering, expand Columns, and select **STATUS_CD**.
    c)	In the property editor, replace the Heading with **Status**. 
    d)	Click Save. Then, click **Save and Run Page**.
    e)	In the interactive report, click a project name.
    f)	In the Developer Toolbar, click **Edit Page 5**.

2.	In the page designer, click the **Processing** tab. 
    Right-click **Validating** and select **Create Validation**.
    ![](images/1_2.png)
    In the central pane, click the **Help** tab.
    **Note**: The help text displays the currently selected attribute in the Property Editor (right pane). For example, clicking on the Validation Type attribute label (not the select list) displays a list of all the available options, together with a description of when each option will pass (not display the error message) or fail (displays the error message). 

3.	In the property editor:
    -	Identification: Name - enter **Completed Date is Not Null**
    -	Validation: Type - select **Item is NOT NULL**
    -	Validation: Item - select **P5_COMPLETED_DATE**
    -	Error: Error Message - select the Error Message attribute label (not the data entry area), at which point the Help pane will display the help text for Error Message. On the Help pane under Examples, copy and paste **#LABEL# must have some value**. into the Property Editor attribute
    -	Server-side Condition: Type - select **Item = Value**
    -	Server-side Condition: Item - select **P5_STATUS_CD**
    -	Server-side Condition: Value - enter **COMPLETED**
    **Note**: This condition ensures that the validation only fires when the Status item is COMPLETED.
    ![](images/1_3a.png)
    ![](images/1_3b.png)
    Note: The #LABEL# text within the Error Message will be substituted with the Label of the associated item. In this manner, if the item label is updated the error message will also reflect the updated value. This improves consistency and prevents messages having an out of date label reference.

4.	In the Processing pane, right-click **Validating** and select **Create Validation**.

5.	In the property editor:
    -	Identification: Name - enter **Completed Date is not Forward Dated**
    -	Validation: PL/SQL Expression - enter :**P5_COMPLETED_DATE <= sysdate**
    -	Error: Error Message - enter **#LABEL# cannot be forward dated**
    -	Error: Associated Item - select **P5_COMPLETED_DATE**
    -	Condition: Type - select **Item is NOT NULL**
    -	Condition: Item - select **P5_COMPLETED_DATE**
    ![](images/1_5a.png)
    ![](images/1_5b.png)

6.	Now that you created the two validations, you want to verify if they work as expected.            Navigate to the Demo Projects application runtime environment.
    In the navigation menu, click **Demo Projects**. Then, select a project name.

7.	Try out these functions to see how the page responds:
    -	Save a record with a Status of COMPLETED and no Completion Date - An error message should be displayed.
    ![](images/1_7a.png)
    -	Save a record with a Completion Date in the future - An error message should be displayed.
    ![](images/1_7b.png)

### HOL 10-2: Creating and Using a Computation

In this lab, you create a computation that changes the Assigned To value entered using the form to uppercase after the page is submitted.

1.	Navigate to **App Builder** and run the **Budget App** application.

2.	In the navigation menu, click **Budget**. This is the interactive report that has been created when you created the application using a spreadsheet in HOL 3-2.

3.	Create an After Submit PL/SQL Expression computation on the P2_ASSIGNED_TO item. The PL/SQL expression should be: **upper(:P2_ASSIGNED_TO)**. Test the page to see that the Assigned To is stored as uppercase.

    Perform the following steps:
    a) In the PROJECT_BUDGET interactive report, click the **Edit** icon (pencil) for any record.
    Then, in the Developer Toolbar, click **Edit Page 3**.
    ![](images/2_3a.png)
    b) In the page designer, click **Page Processing**.
    Right-click **After Submit** and select **Create Computation**.
    ![](images/2_3b.png)
    c) In the property editor:
    -	Identification > Item Name: Select **P3_ASSIGNED_TO**
    -	Execution Options > Point: Select **After Submit**
    -	Computation > Type: Select **PL/SQL Expression**
    d) Computation > PL/SQL Expression: Enter **upper(:P3_ASSIGNED_TO)**
    ![](images/2_3d.png)
    Click **Save**
    e) This is a dialog page and so you cannot run this directly. You need to first run interactive report page. 
    Navigate to application runtime environment and click **Budget** in the navigation menu and then click the edit icon for a record.
    ![](images/2_3e.png)
    f)	Click **Apply Changes**. The data is submitted now.
    g)	Navigate to application runtime environment and click PROJECT_BUDGET in the navigation menu and then click the edit icon for the same record that you did in step e above. Notice that the value for Assigned To is stored in uppercase.
    ![](images/2_3g.png)

### HOL 10-3: Creating and Using a Process

In this lab, you create a process to insert a record into a table called AUDIT_DETAILS every time a project is added.

1.	You want to create an After Submit process on the Budget form page. Whenever a user adds a new project by using this form, the user details are stored in the AUDIT_DETAILS table. 

    Perform the following steps:
    a)	View **Page 3** in page designer
    b)	Click the Processing tab, and navigate to **Processing > Processes**.
    Select **Process form Budget**.
    In the property editor, note that Return Primary Keys) after Insert is **Yes** by default.
    Under Success Message > Success Message: Enter **Project added successfully!**
    Click **Save**.
    ![](images/3_1b.png)

2.	Navigate to SQL Workshop and create the AUDIT_DETAILS table.
    a)	Click **SQL Workshop** and select **SQL Commands**.
    b)	Copy the following SQL and paste it in the SQL Commands area and click **Run**.
    ```
    CREATE table "AUDIT_DETAILS" (
        "ID"         NUMBER,
        "CREATED_BY" VARCHAR2(60),
        "CREATED_ON" DATE,
        constraint  "AUDIT_DETAILS_PK" primary key ("ID")
    )
    ```
    ![](images/3_2b.png)
    c)	The table is created. Now, navigate to the window or tab of the Budget App application runtime environment.
    In the navigation menu, click **Budget**. 
    Click the Edit icon for a record and then in the Developer Toolbar, click **Edit Page 3**.

3.	Click the **Processing** tab. 
    Navigate to Processing, right-click **Processes** and select **Create Process**.
    ![](images/3_3.png)

4.	In the property editor:
    -	Identification > Name: Enter **Audit Details**
    -	Identification > Type: Select **PL/SQL Code**
    -	Source > PL/SQL Code: Copy and paste the following code:
    ```
    INSERT INTO audit_details VALUES(:P3_ID,:APP_USER, sysdate);
    ```
    -	Execution Options > Sequence: Enter **40**
    -	Execution Options > Point: Select **Processing**
    -	Success Message > Success Message: Enter **Success!**
    -	Error > Error Message: Enter **Error!**
    -	Server-side Condition > When Button Pressed: Select **CREATE**
    Click **Save**.
    **Note**: The sequence of this process should be the one immediately after the Process Row of Process form Budget process.
    ![](images/3_4a.png)
    ![](images/3_4b.png)
    Then, click **Save and Run Page**.

5.	Now, you want to verify if the processes are working. In the page designer toolbar, click the Navigate to Previous Page arrow.
    ![](images/3_5.png)

6.	Click the **Create** button. 

7.	In the Budget dialog, enter values for each of the fields and click **Create**.
    -	Project: **New Packaged App**
    -	Task Name: **Prepare requirements doc**
    -	Start Date: **01-Ju1-19**
    -	End Date: **25-Jul-19**
    -  	Status: **Open**
    -	Assigned To: **Pam King**
    -	Cost: **500**
    - 	Budget: **800**
    ![](images/3_7.png)

8.	The record is created now. In the Developer Toolbar, click **Home**.

9.	Click **SQL Workshop**. Then, click **Object Browser**. 
    Under Tables, select **AUDIT_DETAILS**. 
    Click **Data**.
    Notice that the user details have been added to the table.
    ![](images/3_9.png)

### HOL 10-4: Creating and Using Validations

In this lab, you create two validations on the Project Budget form page. The first validation you create ensures that the project field is not null. The second one ensures that the value entered for cost is only numeric.

1.	Navigate to the window or tab of the Budget App application runtime environment.
    In the navigation menu, click **Budget**. 
    Click the Edit icon for a record and then in the Developer Toolbar, click **Edit Page 3**.

2.	You want to create two validations. The first validation is to ensure that the Project field is not null. 
    In the page designer, click the **Processing** tab.
    Right-click **Validating** and select **Create Validation**.
    ![](images/4_2.png)

3.	In the property editor:
    -	Identification > Name: Enter **Project is not null**
    -	Validation > Type: Select **Item is NOT NULL**
    -	Validation > Item: Select **P3_PROJECT**
    -	Error > Error Message: Enter **Project is not null!**
    -	Error > Display Location: Select **Inline in Notification**
    ![](images/4_3.png)

4.	You need to create another validation to ensure that the value entered for Cost should be only numeric.
    Under Processing, right-click **Validating** and select **Create Validation**.

5.	In the property editor:
    -	Identification > Name: Enter **Cost should be numeric**
    -	Validation > Type: Select **Item is numeric**
    -	Validation > Item: Select **P3_COST**
    -	Error > Error Message: Enter **Cost should be numeric**
    -	Error > Display Location: Select **Inline with Field**
    -	Error > Associated Item: Select **P3_COST**
    Click **Save**.
    ![](images/4_5.png)

6.	Now, you can test to verify if the validations work. Navigate to the application run time environment. 
    In the navigation menu, click **Budget**.
    Then, click **Create**.

7.	In the Project Budget dialog, enter the following and then click the **Create** button.
    -	Task Name: **Prepare requirements doc**
    -  	Start Date: **03-Jul-19**
    -	End Date: **25-Jul-19**
    -	Status: **Open**
    -	Assigned To: **Pam King**
    -	Cost: **abcd12**
    -	Budget: **3000**
    ![](images/4_7.png)
    Notice that the errors are displayed. 
    Click **Cancel**.

8.	Navigate to Page Designer. 
    Under Rendering, select **P3_COST** and **P3_BUDGET**.
    In the property editor, for Settings > Number Alignment, select **Left**.
    Click **Save**.
    ![](images/4_8.png)

9.	Navigate to the application run time environment. 
    In the navigation menu, click **Budget**.
    Then, click the edit icon for any project.
    In the Budget form, now you see that the values in the Cost and Budget fields are left aligned.
    ![](images/4_9.png)
    ![](images/last.png)





 


















