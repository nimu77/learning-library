# Module 4: Using Page Designer - Updating the Milestones Page
Now, that you have created a new app with a new milestone page with an interactive grid. 
### **Part 1**: Updating Project Id
1. To replace the Project Id with the Project Name, define an LOV.
  - In the runtime environment, within the developer toolbar, click **Edit Page 4**
- Page Designer will be displayed for the Milestones page
   - In the Rendering tree (left pane), click **Columns**, click **PROJECT_ID**. 

    ![](images/4/page-designer.png)   

- In the Property Editor (right pane), enter the following:
   - Identification > Type – select **Select List**.
   - Heading – enter **Project**.
   - List of Values > Type – select **SQL Query**.
   - SQL Query enter:
   ```   
   select name, id
   from sample$projects
   order by 1
   ```
  - Display Extra Values – select **No**.
  - Null Display Value – enter **- Select Project -**.
- Click **Save**.

    ![](images/4/property-editor.png) 
- Run the application.

### **Part 2**: Manage Columns

- In the runtime environment, click **Actions**, click **Columns**.  
    ![](images/4/edit-milestone.png) 
- Uncheck **Created**, **Created By**, **Updated**, and **Updated By**.
- Select **Due Date**, click the Up Arrow.
- Click **Save**.  
    ![](images/4/action-column.png) 

### **Part 3**: Freeze and Resize Columns

- Click the column heading **Name**.
- Click **Freeze**.  
    ![](images/4/action-freeze.png)
- Hover between the **Project** and **Name** columns until a bar displays.
- Drag to the right until the **Project** resizes to a suitable size.
- Repeat for other columns.  
    ![](images/4/adjust-column.png)

### **Part 4**: Save the Report

- Click **Actions**, select **Report**, click **Save**.
    ![](images/4/save-report.png)

To be added. [Click here to navigate to Module 5](5-creating-a-page-to-update-project-records-add-the-project-form-page.md)
