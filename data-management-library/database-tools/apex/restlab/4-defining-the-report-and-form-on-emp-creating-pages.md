# Module 4: Defining the Report and Form on EMP - Creating Pages

### **Part 1**: Use the Create Page Wizard

- Return to the Application Home Page
- Click **Create Page**

    ![](https://i.imgur.com/XHFg8ij.png[/img])

- For Page Type, click **Report**  
    ![](https://i.imgur.com/Sp9G5Yx.png[/img])
- For Report Type, click **Report and Form**  
    ![](https://i.imgur.com/DzeETaz.png[/img])
- For Report Page Name, enter **Employees**
- For Form Page Name, enter **Maintain Employee**
- For Form Page Mode, click **Modal Dialog**
- For Breadcrumb, select **Breadcrumb**
- Click **Next**

    ![](https://i.imgur.com/oFkJmQn.png[/img])

- For Navigation Preference, click **Create a new navigation menu entry**
- Click **Next**

    ![](https://i.imgur.com/3Xam413.png[/img])
- For Data Source, click **Web Source**
- For Web Source Module, select **REST EMP Source**
- Click **Next**

    ![](https://i.imgur.com/i6FMdky.png[/img])
- For Primary Key Column, select **EMPNO (Number)**
- Click **Create** 

    ![](https://i.imgur.com/jTOysvX.png[/img])

### **Part 2**: Run the Application

- From Page Designer, click **Save and Run**  
![](https://i.imgur.com/CjbVCTb.png[/img])

- On the Login Page, enter your user credentials  
    ![](https://i.imgur.com/EwHUhkp.png[/img])

- Review the Employees

    ![](https://i.imgur.com/JTdTEjb.png[/img])

- On the Employees report page, click **Actions**, click **Columns**  
    ![](https://i.imgur.com/zzHbZfe.png[/img])
- Shuffle the columns to put EMPNO,ENAME, and DEPTNO as the
first three columns, by selecting the column and using the arrows.
- Click **Apply**  
    ![](https://i.imgur.com/ZWot5D0.png[/img])

- Click **Actions**, select **Report**, click **Save Report**  
    ![](https://i.imgur.com/kz1g1Uo.png[/img])

- For Save, select **As Default Report Settings**  
    ![](https://i.imgur.com/5hZ8KBC.png[/img])
- Click **Apply**

    ![](https://i.imgur.com/vD2HnHN.png[/img])
- Click the edit icon on a row - The Form Page is displayed
- In the Developer Toolbar, click **Edit Page 3** 
  - Page Designer will be displayed
for the current page

    ![](https://i.imgur.com/4k4HEkm.png[/img])  
*{Note: The Developer Toolbar is only displayed when you run apps from App Builder, so is never visible to end users}*

### **Part 3**: Update the Page

- In the Rendering tab (left pane), click Column **P3_EMPNO**
- In the Property Editor (right pane)
  - For Type select **Number Field**
   - For Label enter **Empno**

    ![](https://i.imgur.com/duhtkJd.png[/img])
- In the Rendering tab (left pane),
click Column **P3_JOB**
- In the Property Editor (right pane),
for Type select **Text Field**
- In the Rendering tab (left pane),
click Column **P3_ENAME**
- In the Property Editor (right pane),
for Type select **Text Field**
- In the Rendering tree,
drag **P3_ENAME** up to be under **P3_EMPNO**  
    ![](https://i.imgur.com/CI8koHZ.png[/img])
- In the Rendering tab (left pane), click Column **P3_DEPTNO**
- Drag **P3_DEPTNO** up to be under **P3_ENAME**
- In Layout (middle pane),
select **P3_COMM**
- Drag it up next to **P3_SAL**
- In the Toolbar, click **Save**

    ![](https://i.imgur.com/hLDYHbS.png[/img])

### **Part 4**: Insert a Record

- Navigate back to the Runtime environment
- Refresh the browser
- Click **Create**

    ![](https://i.imgur.com/MCCvB51.png[/img])

- For Empno enter **1234**
- For Ename enter **SMITH**
- For Deptno enter **10**
- For Job enter **CLERK**
- For Mgr enter **7839**
- For Sal enter **1500**
- For Hiredate select any date
- Click **Create**
- *Find the new entry on the
Employees report page*

    ![](https://i.imgur.com/kG4ncEF.png[/img])

### **Part 5**: Update a Record

- In the report, find **Ward**, and click the edit icon
- For Sal, enter **1500**
- For Comm, enter **750**
- Click **Apply Changes**
- Review **Ward** in the report

    ![](https://i.imgur.com/RsVS5Ya.png[/img])

### **Part 6**: Delete a Record

- In the report, find **Turner**, and click the edit icon
- Click **Delete**
- Click **Ok**
- *Review the report to
ensure Turner is deleted*

    ![](https://i.imgur.com/KL3OuCp.png[/img])

## Summary

TODO. [Click here ot navigate to Module 5](5-using-the-rest-service-on-dept-defining-list-of-values.md)