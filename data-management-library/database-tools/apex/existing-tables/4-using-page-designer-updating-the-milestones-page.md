## Module 4

## Using Page Designer - Updating the Milestones Page

### **Part 1** - Update Project Id
- To replace the Project Id with the Project Name, define an LOV.
  - In the runtime environment, within the developer toolbar, click **Edit Page 4**
- Page Designer will be displayed for the Milestones page
   - In the Rendering tree (left pane), click **Columns**, click **PROJECT_ID**. 

    ![](images/section5/5.1.PNG)   

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

    ![](images/section5/5.1(1).PNG) 
- Run the application.

### **Part 2** - Manage Columns

- In the runtime environment, click **Actions**, click **Columns**.  
    ![](images/section5/5.2.PNG) 
- Uncheck **Created**, **Created By**, **Updated**, and **Updated By**.
- Select **Due Date**, click the Up Arrow.
- Click **Save**.  
    ![](images/section5/5.2(2).PNG) 

### **Part 3** - Freeze and Resize Columns

- Click the column heading **Name**.
- Click **Freeze**.  
    ![](images/section5/5.3.PNG)
- Hover between the **Project** and **Name** columns until a bar displays.
- Drag to the right until the **Project** resizes to a suitable size.
- Repeat for other columns.  
    ![](images/section5/5.3(1).PNG)

### **Part 4** - Save the Report

- Click **Actions**, select **Report**, click **Save**.
    ![](images/section5/5.4.PNG)

To be added. [Click here to navigate to Module 5](5-creating-a-page-to-update-project-records-add-the-project-form-page.md)
