# Module 5: Using the REST Service on DEPT - Defining List of Values

### Information

When you ran the script in your first workspace you created a REST
handler for the DEPT table. You can now utilize that REST URI within
a PL/SQL Function by using the APEX_EXEC package.

In order to utilize the APEX_EXEC package you must first define a
Web Source on the REST DEPT Service within this application.

Once fully implemented, you can utilize the function as the basis for
a List of Values against the DEPT table.

Read this blog post for more details:  
https://blogs.oracle.com/apex/apex-181-early-adopter-2-rest-services-and-plsql

### **Part 1**: Add Web Source for DEPT

- Return to the Application Builder
- Go to the App Builder Home Page
- Select your application
- Click **Shared Components**
- Click **Web Source Modules**
- From Web Source Modules, click **Create**
- Click **Next** {Default: From Scratch}
- For Web Source Type,
select **ORACLE REST Data Services**
- For Name
enter **REST DEPT Source**
- For URL Endpoint
enter the REST URI for the dept.rest handler
{Similar to https://<<your service>>/dpeake_rest/**dept**/hol/ }
- Click **Next**

    ![](https://i.imgur.com/LrWVF2Y.png[/img])

- Review the Base URL and Service URL Path
- Click **Next**
- Click **Discover**
{Authentication Required = No}
- Click **Create Web Source**

    ![](https://i.imgur.com/eoah4Nm.png[/img])

### **Part 2**: Adding a Function to call DEPT

- In the main menu, select **SQL Workshop**, click **SQL Scripts**  
    ![](https://i.imgur.com/w0xMS99.png[/img])

- Click **Create**  
    ![](https://i.imgur.com/NfzD7se.png[/img])

- Copy the following URL into a new window in your browser:  
  *{Remember you are on Slide 54 if you click the link directly}*
  http://www.oracle.com/technetwork/developer-tools/apex/application-express/apex-hol-func-5478627.txt

- In the Script Editor:
  - Enter Script Name = **DEPT Function**
  - Paste the contents of the file into the body
  - Click **Run**  
    ![](https://i.imgur.com/87Qgaxw.png[/img])

- Click **Run Now**

- Results should show 3 statements processed successfully
    ![](https://i.imgur.com/lPSoev5.png[/img])

### **Part 3**: Add the List of Values

- Return to App Builder
- Select your application
- Click **Shared Components**
- Click **List of Values**

    ![](https://i.imgur.com/UkQjFmr.png[/img])

- Click **Create**
- Click **Next** {Default: From Scratch}
- For Name, enter **DEPT LOV**
- For Type, select **Dynamic**
- Click **Next**

    ![](https://i.imgur.com/WFWo6JQ.png[/img])

- For Query enter  
```
      select dname as d,
             deptno as r
        from table ( dept_rest )
      order by 1
```

![](https://i.imgur.com/zFmY9te.png[/img])  
*Note: dept_rest is the name of the function created in the previous step*
- Click **Create List of Values**

### **Part 4**: Update the EMP Pages

- Click on **Application xxxxx** in the breadcrumbs
- Click 2 - **Employees**

    ![](https://i.imgur.com/Lw2g71v.png[/img])


- In the Rendering tree (left pane), click Columns, click **DEPTNO**  
-  In the Property Editor (right pane)
   - For Type, select **Plain Text (based on List of Values)** 
   - For List of Values, select **DEPT LOV** 
   - For Heading > Alignment, click **Start** 
   - For Layout > Column Alignment, click **Start**
- In the toolbar, click **Save**

    ![](https://i.imgur.com/k6cZaM5.png[/img])

- Navigate to Page 3

![](https://i.imgur.com/QvU32sQ.png[/img])
- In the Rendering tree (left pane), click **P3_DEPTNO**
- In the Property Editor (right pane)
  - For Type, select **Select List** 
  - For List of Values > Type, select **Shared Component** 
  - For List of Values, select **DEPT LOV** 
  - For Display Extra Values, click **No** 
  - For Display Null Value, click **No**
- In the toolbar, click **Save**  

    ![](https://i.imgur.com/crGAkYz.png[/img])

### **Part 5**: Run the Application

- Navigate to the application Runtime Environment
- Refresh your browser

    ![](https://i.imgur.com/5gaYlXS.png[/img])

- Click on the edit icon for any record
- Select a department

    ![](https://i.imgur.com/GEfeilw.png[/img])

## Summary

TODO.

## **Learn More** - *Useful Links*

- APEX on Autonomous https://apex.oracle.com/autonomous
- APEX Collateral https://apex.oracle.com
- Tutorials https://apex.oracle.com/en/learn/tutorials
- Community https://apex.oracle.com/community
- External Site + Slack http://apex.world