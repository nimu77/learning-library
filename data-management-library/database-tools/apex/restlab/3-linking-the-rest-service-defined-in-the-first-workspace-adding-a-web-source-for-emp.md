## Module 4

### Linking the REST Service defined in the first workspace - Adding a Web Source for EMP

### **Part4.1** – Add Web Source for EMP 

- Click **Shared Components**  
![](https://i.imgur.com/G6Ys9Mc.png[/img])
- Under **Data Sources**, click **Web Source Modules**  
![](https://i.imgur.com/DmDC8Y6.png[/img])
- Click **Create**
- Click **Next** {Default: From Scratch}
- For Web Source Type,
select **ORACLE REST Data Services**
- For Name
enter **REST EMP Source**
- For URL Endpoint
enter the REST URI you tested previously
{Similar to https://<<your service>>/dpeake_rest/emp/hol/ }
- Click **Next**

![](https://i.imgur.com/tonnsIx.png[/img])

- Review the Base URL and Service URL Path
- Click **Next**
- Click **Discover**
{Authentication Required = No}
- Click **Create Web Source**

![](https://i.imgur.com/SiqCpPY.png[/img])

### **Part 4.2** – Adding Operations

- Click **REST EMP Source**

![](https://i.imgur.com/KFwpjqU.png[/img])

- Notice only the GET and POST Operations have been added
- Click **Add Operation**

![](https://i.imgur.com/0QWW9za.png[/img])

- For URL Pattern, enter **:empno**
- For HTTP Method, select **GET**
- For Database Operation, select **Fetch single row**
- Click **Create** 

![](https://i.imgur.com/CLtL8Pz.png[/img])

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
![](https://i.imgur.com/57km04W.png[/img])
