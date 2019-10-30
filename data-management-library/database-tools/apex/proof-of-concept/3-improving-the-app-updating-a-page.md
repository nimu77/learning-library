# Module 3: Improving the App - Updating a Page

### **Part 1**: Restart the Create App Wizard

- From the development environment, click **App Builder**, and then select **Create**  
    ![](images/3/app-builder-create.png)

- Click **New Application**

### **Part 2**: Load Blueprint

- In the Create App Wizard, click **Load Blueprint**
- For Projects, click **Load**

    ![](images/3/load-blueprint.png)

### **Part 3**: Add a Page

- Click **Add Page**
- Click **Interactive Grid**

    ![](images/3/add-interactive-grid.png)

- For Page Name, enter **Milestones**
- For Table or View, select **HOL_MILESTONES**
- Click **Add Page**

    ![](images/3/enter-values-interactive-grid.png)

### **Part 4**: Reorder a Page

- Click and hold the mouse when hovering over the hamburger for
the **Milestones – Interactive Grid** page
- Move it up until the page is under Projects
- Release the mouse

    ![](images/3/reorder-pages.png)

### **Part 5**: Delete a Page

- For **Milestones – Interactive Report with Form** page, click **Edit**
- Click **Delete**

    ![](images/3/delete-a-page.png)

### **Part 6**: Create App and Run

- Click **Create Application**
- In Page Designer, click **Run Application**

    ![](images/3/create-app-and-run.png)

### **Part 7**: Navigate to Milestones

- In the runtime environment, click **Milestones**  
    ![](images/3/runtime-milestone.png)
- In the Developer Toolbar, click **Edit Page 6**  
    ![](images/3/edit-page-milestone.png)

### **Part 8**: Update Project ID Column

- In Page Designer, under Milestones, click **Columns**
- Click **PROJECT_ID**

    ![](images/3/update-column.png)

- In the Property Editor, update the following:
   - Identification: Type – select **Select List**
   - Heading: Heading – enter **Project**
   - List of Values: Type – select **Shared Component**
   - List of Values – select **HOL_TASKS.PROJECT_ID.LOOKUP**
   - Display Extra Values – click **No**
   - Display Null Value – click **No**  
    ![](images/3/.png)  - #need a new picture
- Save and Run the App

- In the Property Editor, update the following:
  - Identification: Type – select **Select List**
  - Heading: Heading – enter **Project**
  - List of Values: Type – select **SQL Query**
  - List of Values – SQL Query enter 
  ~~~~sql
  select name d, id r 
  from hol_projects 
  order by 1
  ~~~~
  - Display Extra Values – click **No**
  - Display Null Value – click **No**   
    ![](images/3/update-and-save.png)
- Save and Run the App

### **Part 9**: Hide Columns

- In the runtime environment, click **Actions**, select **Columns**
- Uncheck Displayed for **Id, Row Version, Created, Created By,
Updated**, and **Updated By**
- Click **Save**

    ![](images/3/hide-columns.png)

### **Part 10**: Save the Report

- In the runtime environment, click **Actions**, select **Report**,
select **Save**

    ![](images/3/save-the-report.png)

## **Learn More** *Useful Links*

- **APEX on Autonomous** https://apex.oracle.com/autonomous
- **APEX Collateral** https://apex.oracle.com
- **Tutorials** https://apex.oracle.com/en/learn/tutorials
- **Community** https://apex.oracle.com/community
- **External Site + Slack** http://apex.world