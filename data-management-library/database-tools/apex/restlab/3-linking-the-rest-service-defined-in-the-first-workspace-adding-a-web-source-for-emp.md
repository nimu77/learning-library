# Module 3: Linking the REST Service defined in the first workspace - Adding a Web Source for EMP

### **Part 1**: Add Web Source for EMP 

1. Click **Shared Components**  
    ![](images/3/click-shared-components.png)
2. Under **Data Sources**, click **Web Source Modules**  
    ![](images/3/web-source-modules.png)
3. Click **Create**
4. Click **Next** 
    *Default: From Scratch*
5. For Web Source Type, select **ORACLE REST Data Services**
6. For Name enter **REST EMP Source**
7. For URL Endpoint, enter the REST URI you tested previously
    *Similar to https://<< your service >>/dpeake_rest/emp/hol/*
8. Click **Next**

    ![](images/3/web-source-type.png)

9. Review the Base URL and Service URL Path
10. Click **Next**
11. Click **Discover**
    *Authentication Required = No*
12. Click **Create Web Source**

    ![](images/3/create-web-source.png)

### **Part 2**: Adding Operations

1. Click **REST EMP Source**

    ![](images/3/click-rest-emp-source.png)

2. Notice only the GET and POST Operations have been added
3. Click **Add Operation**

    ![](images/3/click-add-operation.png)

| Property | Type or Select | Value |
| --- | --- | --- |
| URL Pattern | type | **:empno** |
| HTTP Method | select | **PUT** |
| Database Operation | select | **Fetech single row** |
- Click **Create** 

    ![](images/3/select-database-operation.png)

4. Click **Add Operation**

| Property | Type or Select | Value |
| --- | --- | --- |
| URL Pattern | type | **:empno** |
| HTTP Method | select | **PUT** |
| Database Operation | select | **update row** |
- Click **Create**

5. Click **Add Operation**

| Property | Type or Select | Value |
| --- | --- | --- |
| URL Pattern | type | **:empno** |
| HTTP Method | select | **DELETE** |
| Database Operation | select | **Delete row** |
- Click **Create**  
    ![](images/3/operations.png)

## Summary

TODO. [Click here to navigate to Module 4](4-defining-the-report-and-form-on-emp-creating-pages.md)
