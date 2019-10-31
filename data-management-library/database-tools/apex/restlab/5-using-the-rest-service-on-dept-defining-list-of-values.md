# Module 5: Using the REST Service on DEPT - Defining List of Values

### Information

When you ran the script in your first workspace you created a REST handler for the DEPT table. You can now utilize that REST URI within a PL/SQL Function by using the APEX_EXEC package.

In order to utilize the APEX_EXEC package you must first define a Web Source on the REST DEPT Service within this application.

Once fully implemented, you can utilize the function as the basis for a List of Values against the DEPT table.

Read this blog post for more details:  
https://blogs.oracle.com/apex/apex-181-early-adopter-2-rest-services-and-plsql

### **Part 1**: Add Web Source for DEPT

1. Return to the Application Builder.
2. Go to the App Builder Home Page and select your application.
3. Click **Shared Components**.
4. Under Data Sources, Click **Web Source Modules**.
5. From Web Source Modules, click **Create**.
6. Click **Next**.
    *Default: From Scratch*
7. For Web Source Type, select **ORACLE REST Data Services**.
8. For Name enter **REST DEPT Source**
9. For URL Endpoint, enter the REST URI for the dept.rest handler, and then click **Next**.
*Similar to https://<< your service >>/dpeake_rest/**dept**/hol/*

    ![](images/5/web-source-type.png)

10. Review the Base URL, Service URL Path, and then click **Next**.
11. Click **Discover**.
*Authentication Required = No*
12. Click **Create Web Source**.

    ![](images/5/create-web-source.png)

### **Part 2**: Adding a Function to call DEPT

1. In the main menu, select **SQL Workshop**, click **SQL Scripts**  
    ![](images/5/select-sql-scripts.png)

2. Click **Create**  
    ![](images/5/click-create.png)

3. Copy the following URL into a new window in your browser:  
  *Remember you are on Slide 54 if you click the link directly*
  http://www.oracle.com/technetwork/developer-tools/apex/application-express/apex-hol-func-5478627.txt

4. In the Script Editor:
    - Enter Script Name = **DEPT Function**
    - Paste the contents of the file into the body
    - Click **Run**  
    ![](images/5/type-script-name.png)

    - Click **Run Now**
    - Results should show 3 statements processed successfully
    ![](images/5/result-shown.png)

### **Part 3**: Add the List of Values

1. Return to App Builder and select your application.
2. Click **Shared Components**; Click **List of Values**.

    ![](images/5/list-of-values.png)

3. Click **Create**, and then click **Next**.
*For, create list of values, keep Default: From Scratch*
4. For Name, enter **DEPT LOV**.
5. For Type, select **Dynamic**.
6. Click **Next**.

    ![](images/5/name-and-type.png)

7. For Query enter  
    ```
      select dname as d,
             deptno as r
        from table ( dept_rest )
      order by 1
    ```

    ![](images/5/click-create-list-of-values.png)  
    *Note: dept_rest is the name of the function created in the previous step*
8. Click **Create List of Values**.

### **Part 4**: Update the EMP Pages

1. Click on **Application xxxxx** in the breadcrumb, and then click **2 - Employees**

    ![](images/5/click-application-xxxx.png)


2. In the Rendering tree (left pane), click **Columns**, and then click **DEPTNO**.  
    - In the Property Editor (right pane)
        - For Type, select **Plain Text (based on List of Values)** 
        - For List of Values, select **DEPT LOV** 
        - For Heading > Alignment, click **Start** 
        - For Layout > Column Alignment, click **Start**
    - In the toolbar, click **Save**

    ![](images/5/update-column.png)

3. Navigate to Page **3**.

    ![](images/5/navigate-page.png)
4. In the Rendering tree (left pane), click **P3_DEPTNO**.
    - In the Property Editor (right pane).
        - For Type, select **Select List** 
        - For List of Values > Type, select **Shared Component** 
        - For List of Values, select **DEPT LOV** 
        - For Display Extra Values, click **No** 
        - For Display Null Value, click **No**
    - In the toolbar, click **Save**  

    ![](images/5/update-property.png)

### **Part 5**: Run the Application

1. Navigate to the application Runtime Environment and refresh your browser.

    ![](images/5/navigate-to-runtime.png)

2. Click on the edit icon for any record, and select a department.

    ![](images/5/select-list.png)

## Summary

TODO.

## **Learn More** - *Useful Links*

- APEX on Autonomous https://apex.oracle.com/autonomous
- APEX Collateral https://apex.oracle.com
- Tutorials https://apex.oracle.com/en/learn/tutorials
- Community https://apex.oracle.com/community
- External Site + Slack http://apex.world