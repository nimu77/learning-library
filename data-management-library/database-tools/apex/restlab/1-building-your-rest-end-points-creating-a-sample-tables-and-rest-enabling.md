# Module 1: Building your Rest end points - Creating a Sample Tables and REST Enabling

### **Part 1**: Logging In

- Log back into your first workspace
- In the main menu, select **SQL Workshop**, select **Utilities**, click **Sample Datasets** 

    ![](images/1/sample-datasets.png)

### **Part 2**: Creating the EMP and DEPT Tables

- On the EMP /DEPT row, click **Install**  
![](images/1/install-emp-dept.png)
- Click **Next**
- Click **Install Dataset**
- Click **Exit**  
  *We do not want to create an application directly on the tables*

### **Part 3**: REST Enabling the tables

- In the main menu, select **SQL Workshop**, click **SQL Scripts**  
    ![](images/1/select-sql-script.png)
- Click **Create**  
    ![](images/1/click-create.png)
- Copy the following URL into a new window in your browser:
http://www.oracle.com/technetwork/developer-tools/apex/application-express/apex-hol-rest-enable-5478504.txt

In the Script Editor:
  - Enter Script Name = **Manual REST on EMP and DEPT**
  -  Paste the contents of the file into the body
  - Click Run

    ![](images/1/script-name.png)
- Click **Run Now**
- Results should show 4 statements processed successfully

    ![](images/1/scripts-created.png)

### **Part 4**: Reviewing the REST Services

- In the main menu, select **SQL Workshop**, click **RESTful Services**
- Expand **Modules**; Expand **emp.rest**; Click on **GET**
    ![](images/1/copy-url.png)
- Copy the Full URL into your clipboard

### **Part 5**: Testing a REST Service

- Open a new tab / window in your browser
- Paste the Full URL

    ![](images/1/open-url.png)

## Information
Running the SQL Script in Step 3 above REST Enables the schema and also creates modules for the EMP and DEPT tables and the EMP_DEPT_V view, together with the appropriate handlers.

Alternatively, you could have gone directly to SQL Workshop > RESTful Services and REST enabled the schema. Then gone to SQL Workshop > Object Browser, clicked on each table / view and then selected REST to define the REST services. However, the handlers created will utilize Data Dictionary lookups each time they are called. This is less efficient then the manually created services created in Step 3, especially on services such as apex.oracle.com which has over 20,000 schemas and an extremely large data dictionary.

## Summary

TODO.[Click here to navigate to Module 2](2-building-your-app-which-will-be-based-on-the-rest-endpoints-creating-the-app.md)