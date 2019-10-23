# Module 3: Improving the App - Updating a Page

### **Part 3.1**: Restart the Create App Wizard

- From the development environment, click **App Builder**, and then select **Create**  
![](https://i.imgur.com/F0CAdtA.png[/img])

- Click **New Application**

### **Part 3.2**: Load Blueprint

- In the Create App Wizard, click **Load Blueprint**
- For Projects, click **Load**

![](https://i.imgur.com/7XSTr20.png[/img])

### **Part 3.3**: Add a Page

- Click **Add Page**
- Click **Interactive Grid**

![](https://i.imgur.com/Kq1R8CL.png[/img])

- For Page Name,
enter **Milestones**
- For Table or View, select
**HOL_MILESTONES**
- Click **Add Page**

![](https://i.imgur.com/MvavpGO.png[/img])

### **Part 3.4**: Reorder a Page

- Click and hold the mouse when hovering over the hamburger for
the **Milestones – Interactive Grid** page
- Move it up until the page is under Projects
- Release the mouse

![](https://i.imgur.com/TfTn4Mv.png[/img])

### **Part 3.5**: Delete a Page

- For **Milestones – Interactive Report with Form** page, click **Edit**
- Click **Delete**

![](https://i.imgur.com/vzjSc1z.png[/img])

### **Part 3.6**: Create App and Run

- Click **Create Application**
- In Page Designer, click **Run Application**

![](https://i.imgur.com/CGbb0t1.png[/img])

### **Part 3.7**: Navigate to Milestones

- In the runtime environment, click **Milestones**  
![](https://i.imgur.com/3E0HN6u.png[/img])
- In the Developer Toolbar, click **Edit Page 6**  
![](https://i.imgur.com/pu8QZ3m.png[/img])

### **Part 3.8**: Update Project ID Column

- In Page Designer, under Milestones, click **Columns**
- Click **PROJECT_ID**

![](https://i.imgur.com/hyzTFq6.png[/img])

- In the Property Editor, update the following:
   - Identification: Type – select **Select List**
   - Heading: Heading – enter **Project**
   - List of Values: Type – select **Shared Component**
   - List of Values – select **HOL_TASKS.PROJECT_ID.LOOKUP**
   - Display Extra Values – click **No**
   - Display Null Value – click **No**  
![](https://i.imgur.com/HLAIgdT.png[/img])
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
![](https://i.imgur.com/fcUYtLE.png[/img])
- Save and Run the App

### **Part 3.9**: Hide Columns

- In the runtime environment, click **Actions**, select **Columns**
- Uncheck Displayed for **Id, Row Version, Created, Created By,
Updated**, and **Updated By**
- Click **Save**

![](https://i.imgur.com/pAqSeax.png[/img])

### **Part 3.10**: Save the Report

- In the runtime environment, click **Actions**, select **Report**,
select **Save**

![](https://i.imgur.com/xvAVJPG.png[/img])

## **Learn More** *Useful Links*

- **APEX on Autonomous** https://apex.oracle.com/autonomous
- **APEX Collateral** https://apex.oracle.com
- **Tutorials** https://apex.oracle.com/en/learn/tutorials
- **Community** https://apex.oracle.com/community
- **External Site + Slack** http://apex.world