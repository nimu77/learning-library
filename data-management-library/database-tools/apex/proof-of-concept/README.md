# Building a Proof-of-concept for Oracle Autonomous Cloud Service

This lab starts with a napkin design of data structures we would like to use for a proof-of-concept. Using Quick SQL you will quickly define the data structures and utilize various table and column directives to better define the tables and also create some dummy data. You will then be creating an application based on the new tables. Lastly, you will be updating some of the generated components to improve the initial app.

*From napkin design to demo-ready, proof-of-concept app, complete with some dummy data, in minutes - Viola!*


## Lab Objectives

* TODO


## Lab Modules

| # | Module | Est. Time |
| --- | --- | --- |
| 1 | [Using Quick SQL](1-defining-new-data-structures-using-quick-sql.md) | 4 min |
| 2 | [Using the Create Application Wizard](2-creating-an-app-on-the-tables-from-quick-sql-using-the-create-application-wizard.md) | 10 min |
| 3 | [Updating a Page](3-improving-the-app-updating-a-page.md) | 5 min |


## Parts

### **Part 1**: Acquire an Oracle Cloud trial account

In this part, you will create an Oracle Cloud trial account. If you already have an Oracle Cloud account, you may skip to Part 2.

1.  Please [click this link to create your free account](https://myservices.us.oraclecloud.com/mycloud/signup?language=en&sourceType). When you complete the registration process you'll receive an account with a $300 credit and several "forever free" services that will enable you to complete the lab for free. You can then use any remaining credit to continue to explore the Oracle Cloud. The forever free services will continue to work after the trial expires.

2.  Soon after requesting your trial you will receive the following email. Once you receive this email you can proceed to Part 2.

    ![](images/0/get-started-email.png)

### **Part 2**: Log in to your Oracle Cloud account

In this part, you will log into your Oracle Cloud account so that you can start working with various services.

1. Once you receive the **Get Started Now with Oracle Cloud** email, make note of your **Username**, **Password**, and **Cloud Account Name**.

2. From any browser go to https://cloud.oracle.com/en_US/sign-in.

3. Enter your **Cloud Account Name** in the input field and click the **Next** button.

    ![](images/0/enter-oracle-cloud-account-name.png)

4. Enter your **Username** and **Password** in the input fields and click **Sign In**.

    ![](images/0/enter-user-name-and-password.png)

### **Part 3**: Create an Autonomous Transaction Processing instance

In this part, you will create an instance of the Autonomous Transaction Processing database service.

1. From the Cloud Dashboard, select the navigation menu icon in the upper left-hand corner and then select **Autonomous Transaction Processing**.

    ![](images/0/select-atp-in-nav-menu.png)

2. Click **Create Autonomous Database**.

    ![](images/0/click-create-autonomous-database.png)

3. Select the **Always Free** option, enter **```SecretPassw0rd```** for the ADMIN password, then click **Create Autonomous Database**.

    ![](images/0/atp-settings-1.png)
    ![](images/0/atp-settings-2.png)
    ![](images/0/atp-settings-3.png)

    After clicking **Create Autonomous Database**, you will be redirected to the Autonomous Database Details page for the new instance. Continue to the next part when the status changes from:

    ![](images/0/status-provisioning.png)
    
    to:

    ![](images/0/status-available.png)

### **Part 4**: Create a new workspace in APEX

When you first access APEX you will need to log in as an APEX instance administrator to create a workspace. A workspace is a logical domain where you define APEX applications. Each workspace is associated with one or more database schemas (database users) which are used to store the database objects, such as tables, views, packages, and more. These database objects are generally what APEX applications are built on top of.

1. Click the **Tools** button.

    ![](images/0/click-atp-service-console.png)

2. Click **Open APEX** to access Apex.

    ![](images/0/click-oracle-apex.png)

3. Enter the password for the Administration Services and click **Sign In to Administration**. The password is the same as the one entered for the ADMIN user when creating the ATP instance: **```SecretPassw0rd```**

    ![](images/0/log-in-as-admin.png)

4. Click **Create Workspace**.

    ![](images/0/welcome-create-workspace.png)

5. Enter the following details and click **Create Workspace**.

    | Property | Value |
    | --- | --- |
    | Database User | DEMO |
    | Password | **`SecretPassw0rd`** |
    | Workspace Name | DEMO |

    ![](images/0/create-workspace.png)

6. Click the **DEMO** link in the success message. This will log you out of APEX administration so that you can log into your new workspace.

    ![](images/0/log-out-from-admin.png)

7. Enter **``SecretPassw0rd``** for the password, check the **Remember workspace and username** checkbox, and then click **Sign In**.

    ![](images/0/log-in-to-workspace.png)
    
## Summary

This completes the lab setup. At this point, you know how to create a new Autonomous Transaction Processing instance and create an APEX workspace within it. [Click here to navigate to Module 1](1-defining-new-data-structures-using-quick-sql.md)
