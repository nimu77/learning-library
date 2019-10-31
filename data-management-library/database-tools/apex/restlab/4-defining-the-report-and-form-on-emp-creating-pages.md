# Module 4: Defining the Report and Form on EMP - Creating Pages

### **Part 1**: Use the Create Page Wizard

- Return to the Application Home Page
- Click **Create Page**

    ![](images/4/select-create-page.png)

- For Page Type, click **Report**  
    ![](images/4/click-report.png)
- For Report Type, click **Report and Form**  
    ![](images/4/click-report-with-form.png)
- For Report Page Name, enter **Employees**
- For Form Page Name, enter **Maintain Employee**
- For Form Page Mode, click **Modal Dialog**
- For Breadcrumb, select **Breadcrumb**
- Click **Next**

    ![](images/4/page-attributes.png)

- For Navigation Preference, click **Create a new navigation menu entry**
- Click **Next**

    ![](images/4/select-navigation-entries.png)
- For Data Source, click **Web Source**
- For Web Source Module, select **REST EMP Source**
- Click **Next**

    ![](images/4/select-sources.png)
- For Primary Key Column, select **EMPNO (Number)**
- Click **Create** 

    ![](images/4/primary-key-column.png)

### **Part 2**: Run the Application

- From Page Designer, click **Save and Run**  
    ![](images/4/save-and-run-app.png)

- On the Login Page, enter your user credentials  
    ![](images/4/enter-credentials.png)

- Review the Employees

    ![](images/4/review-employees.png)

- On the Employees report page, click **Actions**, click **Columns**  
    ![](images/4/click-action-column.png)
- Shuffle the columns to put EMPNO,ENAME, and DEPTNO as the
first three columns, by selecting the column and using the arrows.
- Click **Apply**  
    ![](images/4/apply-changes.png)

- Click **Actions**, select **Report**, click **Save Report**  
    ![](images/4/save-report.png)

- For Save, select **As Default Report Settings**  
    ![](images/4/as-default-report-settings.png)
- Click **Apply**

    ![](images/4/click-apply.png)
- Click the edit icon on a row - The Form Page is displayed
- In the Developer Toolbar, click **Edit Page 3** 
  - Page Designer will be displayed
for the current page

    ![](images/4/click-edit-page-three.png)  
*Note: The Developer Toolbar is only displayed when you run apps from App Builder, so is never visible to end users*

### **Part 3**: Update the Page

- In the Rendering tab (left pane), click Column **P3_EMPNO**
- In the Property Editor (right pane)
  - For Type select **Number Field**
   - For Label enter **Empno**

    ![](images/4/update-the-page.png)
- In the Rendering tab (left pane), click Column **P3_JOB**
- In the Property Editor (right pane), for Type select **Text Field**
- In the Rendering tab (left pane), click Column **P3_ENAME**
- In the Property Editor (right pane), for Type select **Text Field**
- In the Rendering tree, drag **P3_ENAME** up to be under **P3_EMPNO**  
    ![](images/4/drag-column.png)
- In the Rendering tab (left pane), click Column **P3_DEPTNO**
- Drag **P3_DEPTNO** up to be under **P3_ENAME**
- In Layout (middle pane), select **P3_COMM**
- Drag it up next to **P3_SAL**
- In the Toolbar, click **Save**

    ![](images/4/save-the-updates.png)

### **Part 4**: Insert a Record

- Navigate back to the Runtime environment
- Refresh the browser
- Click **Create**

    ![](images/4/click-create-on-runtime.png)

- For Empno enter **1234**
- For Ename enter **SMITH**
- For Deptno enter **10**
- For Job enter **CLERK**
- For Mgr enter **7839**
- For Sal enter **1500**
- For Hiredate select any date
- Click **Create**
    *Find the new entry on the Employees report page*

    ![](images/4/enter-values.png)

### **Part 5**: Update a Record

- In the report, find **Ward**, and click the edit icon
- For Sal, enter **1500**
- For Comm, enter **750**
- Click **Apply Changes**
- Review **Ward** in the report

    ![](images/4/update-a-record.png)

### **Part 6**: Delete a Record

- In the report, find **Turner**, and click the edit icon
- Click **Delete**
- Click **Ok**
- *Review the report to
ensure Turner is deleted*

    ![](images/4/delete-a-record.png)

## Summary

TODO. [Click here ot navigate to Module 5](5-using-the-rest-service-on-dept-defining-list-of-values.md)