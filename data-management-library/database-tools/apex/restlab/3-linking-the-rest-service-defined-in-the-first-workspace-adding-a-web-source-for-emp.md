# Module 3: Linking the REST Service defined in the first workspace - Adding a Web Source for EMP

### **Part 1**: Add Web Source for EMP 

- Click **Shared Components**  
    ![](images/3/click-shared-components.png)
- Under **Data Sources**, click **Web Source Modules**  
    ![](images/3/web-source-modules.png)
- Click **Create**
- Click **Next** 
    *Default: From Scratch*
- For Web Source Type, select **ORACLE REST Data Services**
- For Name enter **REST EMP Source**
- For URL Endpoint, enter the REST URI you tested previously
    *Similar to https://<< your service >>/dpeake_rest/emp/hol/*
- Click **Next**

    ![](images/3/web-source-type.png)

- Review the Base URL and Service URL Path
- Click **Next**
- Click **Discover**
    *Authentication Required = No*
- Click **Create Web Source**

    ![](images/3/create-web-source.png)

### **Part 2**: Adding Operations

- Click **REST EMP Source**

    ![](images/3/click-rest-emp-source.png)

- Notice only the GET and POST Operations have been added
- Click **Add Operation**

    ![](images/3/click-add-operation.png)

- For URL Pattern, enter **:empno**
- For HTTP Method, select **GET**
- For Database Operation, select **Fetch single row**
- Click **Create** 

    ![](images/3/select-database-operation.png)

- Click **Add Operation**

  - For URL Pattern, enter :**empno**
  - For HTTP Method, select **PUT**
  - For Database Operation, select **Update row**
  - Click **Create**

- Click **Add Operation**

   - For URL Pattern, enter :**empno**
   - For HTTP Method, select **DELETE**
   - For Database Operation,select **Delete row**
   - Click **Create**  
    ![](images/3/operations.png)

   ## Summary

   TODO. [Click here to navigate to Module 4](4-defining-the-report-and-form-on-emp-creating-pages.md)
