# Module 4: Defining the Report and Form on EMP - Creating Pages

### **Part 1**: Use the Create Page Wizard

1. Return to the Application Home Page
2. Click **Create Page**

    ![](images/4/select-create-page.png)

3. For Page Type, click **Report**  
    ![](images/4/click-report.png)
4. For Report Type, click **Report and Form**  
    ![](images/4/click-report-with-form.png)
5. For Report Page Name, enter **Employees**
6. For Form Page Name, enter **Maintain Employee**
7. For Form Page Mode, click **Modal Dialog**
8. For Breadcrumb, select **Breadcrumb**
9. Click **Next**

    ![](images/4/page-attributes.png)

10. For Navigation Preference, click **Create a new navigation menu entry**
11. Click **Next**

    ![](images/4/select-navigation-entries.png)
12. For Data Source, click **Web Source**
13. For Web Source Module, select **REST EMP Source**
14. Click **Next**

    ![](images/4/select-sources.png)
15. For Primary Key Column, select **EMPNO (Number)**
16. Click **Create** 

    ![](images/4/primary-key-column.png)

### **Part 2**: Run the Application

1. From Page Designer, click **Save and Run**  
    ![](images/4/save-and-run-app.png)

2. On the Login Page, enter your user credentials  
    ![](images/4/enter-credentials.png)

3. Review the Employees

    ![](images/4/review-employees.png)

4. On the Employees report page, click **Actions**, click **Columns**  
    ![](images/4/click-action-column.png)
5. Shuffle the columns to put **EMPNO**, **ENAME**, and **DEPTNO** as the first three columns, by selecting the column and using the arrows.
6. Click **Apply**  
    ![](images/4/apply-changes.png)

7. Click **Actions**, select **Report**, click **Save Report**  
    ![](images/4/save-report.png)

8. For Save, select **As Default Report Settings**  
    ![](images/4/as-default-report-settings.png)
9. Click **Apply**

    ![](images/4/click-apply.png)
10. Click the edit icon on a row - The Form Page is displayed
11. In the Developer Toolbar, click **Edit Page 3** 
    - Page Designer will be displayed for the current page

    ![](images/4/click-edit-page-three.png)  
*Note: The Developer Toolbar is only displayed when you run apps from App Builder, so is never visible to end users*

### **Part 3**: Update the Page

1. In the Rendering tab (left pane), click Column **P3_EMPNO**
2. In the Property Editor (right pane)
    - For Type select **Number Field**
    - For Label enter **Empno**

    ![](images/4/update-the-page.png)
3. In the Rendering tab (left pane), click Column **P3_JOB**
4. In the Property Editor (right pane), for Type select **Text Field**
5. In the Rendering tab (left pane), click Column **P3_ENAME**
6. In the Property Editor (right pane), for Type select **Text Field**
7. In the Rendering tree, drag **P3_ENAME** up to be under **P3_EMPNO**  
    ![](images/4/drag-column.png)
8. In the Rendering tab (left pane), click Column **P3_DEPTNO**
9. Drag **P3_DEPTNO** up to be under **P3_ENAME**
10. In Layout (middle pane), select **P3_COMM**
11. Drag it up next to **P3_SAL**
12. In the Toolbar, click **Save**

    ![](images/4/save-the-updates.png)

### **Part 4**: Insert a Record

1. Navigate back to the Runtime environment
2. Refresh the browser
3. Click **Create**, and enter the following:

    ![](images/4/click-create-on-runtime.png)

| Property | Enter or Select | Values |
| --- | --- | --- |
| Empno | enter | **1234** |
| Ename | enter | **SMITH** |
| Deptno | enter | **10** |
| Jpb | enter | **CLERK** |
| Mgr | enter | **7839** |
| Sal | enter | **1500** |
| Hiredate | select | *any date* |
  
- Click **Create**
    *Find the new entry on the Employees report page*
    ![](images/4/enter-values.png)

### **Part 5**: Update a Record

1. In the report, find **Ward**, and click the edit icon

| Property | Enter or Select | Values |
| --- | --- | --- |
| Sal | enter | **1500** |
| Comm | enter | **750** |

- Click **Apply Changes**
- Review **Ward** in the report
    ![](images/4/update-a-record.png)

### **Part 6**: Delete a Record

1. In the report, find **Turner**, and click the edit icon
2. Click **Delete**
3. Click **Ok**
4. *Review the report to ensure Turner is deleted*

    ![](images/4/delete-a-record.png)

## Summary

TODO. [Click here ot navigate to Module 5](5-using-the-rest-service-on-dept-defining-list-of-values.md)