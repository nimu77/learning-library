# Module 6: Improving Usability - Updating the Task Pages

### **Part 1: Improving the Report**

1. In the runtime environment, within the Navigation Menu, click **Tasks**.
2. In the Development Toolbar (bottom of the screen), click **Edit Page 5**.

    ![](images/6/edit-page-five.png)

3. In Page Designer, within the Rendering tree (left panel), under **Project Tasks** region, click **Columns**, and then click **IS_COMPLETE_YN**.
4. In the Property Editor (right pane), for Heading enter **Complete?**, and then click **Save**.
    ![](images/6/rename-columns.png)
5. Click **Run** icon. Your **Tasks** page should look like this.
    ![](images/6/new-name-columns.png)

### **Part 2: Updating Is Complete**
1. In the runtime environment, click the edit icon for a Tasks, and in the Development Toolbar (bottom of the screen), click **Edit Page 6**.
    ![](images/6/edit-page-six.png)

2. In the Rendering tree (left panel), click **P6_IS_COMPLETE_YN**.
3. In the Property Editor (right pane), for Label > Label enter **Complete?**.

    ![](images/6/updating-page-six.png)

### **Part 3: Creating the Audit Details Region**

The Created, Created By, Updated, and Updated By columns are hidden right now. By, creating a audit details region, it can be moved into a collapsible region and made display only as they are maintained by a trigger on the table.
1. Right-click on **Project Tasks** under **Content Body**, and then click **Create Sub Region**.

    ![](images/6/create-sub-region.png)

2. In the Property Editor (right pane), enter the following:
   - Identification > Title enter **Audit Details**.
   - Appearance > Template select **Collapsible**.

    ![](images/6/update-identification.png)

### **Part 4: Moving the audit columns**

1. In the rendering tree (left pane), select **P6_CREATED**, hold the **< Shift >** key and click **P6_CREATED_BY**,**P6_UPDATED**, and **P6_UPDATED_BY**.
2. In the Property Editor (right pane), enter the following and click **Save**.
   - Identification > Type select **Display Only**.
   - Layout > Region select **..Audit Details**.

    ![](images/6/display-only-column.png)

### **Part 5: Reviewing the Page**

1. Navigate back to the runtime environment, and refresh the browser.
2. Click the edit icon for a Task.  

    ![](images/6/review-the-page.png)

TODO. [Click here to navigate to Module 7](7-linking-pages-link-the-calendar-to-the-tasks-form-pages.md)
