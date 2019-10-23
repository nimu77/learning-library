# Module 2: Defining new data structures - Using Quick SQL

## Oracle Spreadsheet Table
![](https://i.imgur.com/8TkzNms.png[/img])

## Napkin Design - Improved data model for Projects
![](https://i.imgur.com/l8LEEtn.png[/img])

### **Part 2.1** - Open Quick SQL
- Log into your workspace
- Click **SQL Workshop**
- Click **SQL Scripts**
![](https://i.imgur.com/4TBd8Rf.png[/img])
- Click **Quick SQL**
![](https://i.imgur.com/Gdublvv.png[/img])

### **Part 2.2**: Enter shorthand for Team Members table
- Enter the Table Name {Team Members}
- Indent 2 or more spaces and enter the column names

![](https://i.imgur.com/CulnRgR.png[/img])  
*Note: You don’t need to enter all of the column names shown,
as you will load a complete script later in this lesson*

### **Part 2.3**: Enter details for Projects table
- Enter the Table Name in the first column {Projects}
- Indent 2 or more spaces and enter the column names

![](https://i.imgur.com/jtu2T6K.png[/img])

### **Part 2.4**: Review Help

- Click **Help**
- Click **Table Directives**

![](https://i.imgur.com/55CTUHD.png[/img])

- Click **Column Directives**

![](https://i.imgur.com/pV4Sw3X.png[/img])

- Click **Data Types**

![](https://i.imgur.com/6p8xUN6.png[/img])

### **Part 2.5**: Improve the Shorthand

- Close **Help**
- Enter **/insert xx** for tables
- Enter **/nn** for mandatory columns
- Enter **/references team_members** for project lead column
- Enter **num** for budget column
- Enter **/vc30** and **/check ASSIGNED,
IN-PROGRESS, COMPLETED** for
status column

![](https://i.imgur.com/C6zTGtJ.png[/img])

### **Part 2.6**: Enter details for a child table

- Enter the Table Name indented
{Milestones}  
![](https://i.imgur.com/IEYZU5c.png[/img])

- Indent 2 or more spaces and
enter the column names  
![](https://i.imgur.com/qt8TUXO.png[/img])

### **Part 2.7**: Enter details for another child table

- Enter the Table Name indented
{Tasks}
- Indent 2 or more spaces and
enter the column names

![](https://i.imgur.com/VYYEL8e.png[/img])

### **Part 2.8**: Complete the Shorthand

- Copy the following URL into a new window in your browser:
{Remember you are on Part 2.10 if you click the link directly}  
https://www.oracle.com/technetwork/developer-tools/apex/application-express/apex-beginner-quicksql-5095785.txt
- Copy and Paste the full script
into the **Quick SQL Shorthand pane**
- Click **Generate SQL**

![](https://i.imgur.com/9lW6S17.png[/img])

### **Part 2.9**: Update the Settings

- Click **Settings**
- Object Prefix, enter **hol**
- On Delete, select **Restrict**
- Primary Keys, select **12c Identity Data Types**
- Date Data Type, select **TIMESTAMP WITH LOCAL TIME ZONE**
- Audit Columns, check Include
- Row Version Number, check Include
- Click **Save Changes**

![](https://i.imgur.com/nZVvx71.png[/img])

### **Part 2.10**: Save, Review, and Run the Script

- Click **Save SQL Script**
- For Script Name, enter **hol**
- Click **Save Script**
- Click **Review** and **Run**

![](https://i.imgur.com/e2I6k3z.png[/img])  
*Note: The script will be displayed in
the Script Editor within SQL Scripts*
- Click **Run**
- Click **Run Now**  
![](https://i.imgur.com/CyYXjko.png[/img])