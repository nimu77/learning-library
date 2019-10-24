![](images/14/1a.PNG)

**Oracle Application Express: Developing Database Web Applications**

**Hands-On-Labs Guide**

*Unit 14: Adding Additional Pages to your Application*

This exercise includes six hands-on-labs and uses the Demo Projects application.

**HOL 14-1 Creating and Customizing a Calendar**: In this lab, you add a Calendar in the Demo Projects application. Later, you edit the calendar attributes and enable the drag and drop functionality.

**HOL 14-2 Modifying the Dashboard Page**: In this hands-on lab, you first create a blank page named Reports. You select Reports as the Parent Navigation Menu Entry when you create the My Outstanding Tasks and the Project Tree page in this application. 

**HOL 14-3 Updating the Project Tasks Chart**: The Project Tasks chart has already been created in the Dashboard page. This lab covers updating the Project Tasks chart to review the completed and incomplete tasks. 

**HOL 14-4 Adding the Project Milestones Chart**: In this lab, you create the Project Milestones chart to depict past milestones and future milestones. You create a copy of the Project Tasks chart and then edit the chart attributes including the source query.

**HOL 14-5 Adding the Project Status Chart**: In this hands-on lab you create the Project Status chart to depict the completed, in-progress and assigned status of the projects. 

**HOL 14-6 Adding the Project Tree**: In this hands-on lab you create a blank page and then create a Tree region. To perform the steps in this lab, you need the Project_Tree.sql file which is included in the apex-course-labs.zip.


The instructions in this exercise use the following page numbers:
-	Page 12: Reports
-	Page 16: Project Tree


### HOL 14-1: Creating and Customizing a Calendar

In this hands-on lab, you first add a Calendar in the Demo Projects application. Later, you enhance the calendar by adding the drag and drop functionality.

1.	Navigate to **App Builder** and in the report, click **Demo Projects** application. 

2.	In the application home page, click **Create Page**.

3.	Select **Calendar** page type and click **Next**.

    ![](images/14/1_3.png)

4.	Enter **Calendar** for Page Name, select **Breadcrumb** for Breadcrumb, and click **Next**.
    
    ![](images/14/1_4.png)

5.	For Navigation Preference, select the **Create a new navigation menu entry** radio button.
    Click **Next**.

    ![](images/14/1_5.png)

6.	Select **Table** for Source Type, **DEMO_PROJ_TASKS** for Table/View Name.
    Click **Next**.

    ![](images/14/1_6.png)

7.	Select **NAME** for Display Column, and **END_DATE** for End Date Column.
    Click **Create**.

    ![](images/14/1_7.png)

8.	Click **Save and Run Page**.
    In the Developer Toolbar, click **Edit Page 11**.

    ![](images/14/1_8.png)

9.	The Calendar page displays the region title Calendar, and also has a border around the region. 
    In the Rendering tree, locate the Calendar region. Click **Calendar**.
    In the Property Editor, click the **Template Options** button. 

    ![](images/14/1_9.png)

10.	In the Template Options dialog, input the following:
    -	Header - select **Hidden but accessible**
    -	Style - select **Remove UI Decoration**
    Click **OK**.

    ![](images/14/1_10.png)

11.	Click **Save and Run Page**.
    In the Developer Toolbar, click **Application < n >**.

    ![](images/14/1_11.png)

12.	You want to update the navigation menu. In the application home page, click **Shared Components**.

13.	Under Navigation, click **Lists**.

14.	Under Lists, click **Desktop Navigation Menu**.

    ![](images/14/1_14.png)

15.	Under List Details, click **Calendar**.

    ![](images/14/1_15.png)

16.	On the Calendar list entry, for Image/Class enter **fa-calendar**. 
    Click **Apply Changes**.

    ![](images/14/1_16.png)

17.	In the Application Express toolbar, click **Run Page 11**.

    ![](images/14/1_17.png)

18.	In the navigation menu, notice the new icon. In the Developer Toolbar, click **Edit Page 11**.

    ![](images/14/1_18.png)

19.	You need to add the Create and View / Edit links. In the Rendering tree, locate the **Calendar** region. 
    Click **Attributes** under the Calendar region.
    In the Property Editor, locate **Create Link** and click **No Link Defined**.

    ![](images/14/1_19.png)

20.	In the Link Builder – Create Link dialog, select **9** for Page, and enter **9** for Clear Cache.
    Click **OK**.

21.	In the Property Editor, locate **View/Edit Link** and click **No Link Defined**.

22.	In the Link Builder – View / Edit Link dialog, input the following:
    -	Page - select **9 - Maintain Task**
    -	Name - select **P9_ID**
    -	Value - select **ID** or enter **&ID**.
    -	Clear Cache - enter **9**
    Click **OK**.

    ![](images/14/1_22.png)

23.	You can enable calendar drag and drop by using the component attribute Drag and Drop. Your SQL query must select a primary key column and you must have set the Primary Key Column calendar attribute. Then enter the PL/SQL code to update the event row in the database in the Drag and Drop PL/SQL Code attribute. That PL/SQL code typically performs a SQL update on the database table - the bind variables :APEX$PK_VALUE., :APEX$NEW_START_DATE and :APEX$NEW_END_DATE contain the dragged events primary key value as well as the new start and new end timestamp.
    -	In the property editor, navigate to Primary Key Column, and select **ID**.
    -	Select **Yes** for Enable Drag and Drop.
    -	For Drag and Drop PL/SQL Code, copy and paste the following code:

    ```
    begin
    update DEMO_PROJ_TASKS
       set start_date = to_date(:APEX$NEW_START_DATE, 'YYYYMMDDHH24MISS'),
           end_date = to_date(:APEX$NEW_END_DATE, 'YYYYMMDDHH24MISS')
     where ID = :APEX$PK_VALUE;
    end;
    ```
    Then, Click **Save**.

    ![](images/14/1_23.png)

24.	Click **Save and Run Page**.
    Notice that you can now drag and drop tasks in the calendar.
    In the Developer Toolbar, click **Application< n >**.

    ![](images/14/1_24.png)

### HOL 14-2: Modifying the Dashboard Page

In this hands-on lab, first you create a blank page named Reports. You select Reports as the Parent Navigation Menu Entry for the My Outstanding Tasks report and the Tree page you create in the Demo Projects application.

You move the My Outstanding Tasks report region in the Dashboard to a new page.

1.	First, create a blank page in the Demo Projects application. In the application home page, click **Create Page**.

2.	Select **Blank Page** and click **Next**.

3.	Enter **Reports** for Name, select **Breadcrumb** for Breadcrumb, and click **Next**.

    ![](images/14/2_3.png)

4.	Select **Create a new navigation menu entry** for Navigation Preference.
    Click **Next**.

5.	On the confirmation page, click **Finish**.

6.	In the page designer toolbar, click **Shared Components**. (not Page Shared Components).

    ![](images/14/2_6.png)

7.	Under Navigation, select **Lists**.

8.	Under Lists, select **Desktop Navigation Menu**.

9.	Under List Details, select **Reports**.

    ![](images/14/2_9.png)

10.	For Image/Class, enter **fa-table**.
    Click **Apply Changes**.

    ![](images/14/2_10.png)

11.	In the Application Express toolbar, click **Run Page < n >**.

    ![](images/14/2_11.png)

12.	Notice the icon for Reports in the navigation menu.
    Now you add charts and reports to the Demo Projects application. 
    In the Developer Toolbar, click **Application < n >**.

    ![](images/14/2_12.png)

13.	In the application home page, click **Create Page**.

14.	Select **Blank Page** and click **Next**.

15.	Enter **My Outstanding Tasks** for Name, select **Breadcrumb** for Breadcrumb, **Reports** for Parent Entry, and click **Next**.

    ![](images/14/2_15.png)

16.	Select **Create a new navigation menu entry** for Navigation Preference.
    Select **Reports** for Parent Navigation Menu Entry.
    Click **Next**.

    ![](images/14/2_16.png)

17.	On the confirmation page, click **Finish**.

18.	Navigate to application runtime environment and click **Dashboard**.

    ![](images/14/2_18.png)

19.	In the Developer Toolbar, click **Edit Page 10**.

20.	Under Rendering, right-click **My Outstanding Tasks** classic report region and select **Copy Region**.

    ![](images/14/2_20.png)

21.	For To Page, select the page number of the blank page that you created in step 13 above.
    Click **Next**.

    ![](images/14/2_21.png)

22.	Make sure the Region Name is **My Outstanding Tasks** and click **Copy**.

    ![](images/14/2_22.png)

23.	Under Rendering, right-click **My Outstanding Tasks** region and select **Delete**.
    Click **Save**.

    ![](images/14/2_23.png)

24.	In the page designer, navigate to the page on to which you just copied the My Outstanding Tasks classic report region.

    ![](images/14/2_24.png)

25.	Click **Save and Run Page**.

26.	You now see the My Outstanding Tasks classic report. In the Developer Toolbar, click **Edit Page < n >**.
  
    ![](images/14/2_26.png)

27.	Under Rendering, select **My Outstanding Tasks** region.
    In the property editor, under Appearance, click **Template Options**.

    ![](images/14/2_27.png)

28.	For Header, select **Hidden** and click **OK**.

    ![](images/14/2_28.png)

29.	Click **Save and Run Page**.

30.	Now, you see the updated classic report region.

    ![](images/14/2_30.png)

31.	In the navigation menu, click **Dashboard**.

### HOL 14-3: Updating the Project Tasks Chart

In this hands-on lab, you update the Project Tasks Chart in the Dashboard page.

1.	In the Developer Toolbar, click **Edit Page 10**.

2.	Under Rendering, select the Project Tasks region. 
    In the property editor, under Identification, for Title, enter **Tasks Review**.

    ![](images/14/3_2.png)

3.	Under Rendering, expand **Axes** and select **x**.
    In the property editor, under Identification, for Title, enter **Projects**. 
    Click **Save and Run Page**.

    ![](images/14/3_3.png)

4.	In the Developer Toolbar, click **Edit Page 10**.

    ![](images/14/3_4.png)

### HOL 14-4: Adding the Project Milestones Chart

In this hands-on lab, you create a bar chart to show the past and future milestones. You add this chart in to the Dashboard page.

1.	In the Page Designer, under Layout, right-click the **Tasks Review** region, and select **Copy To > Content Body > Tasks Review > Column After**.

    ![](images/14/4_1.png)

2.	The chart region is now copied. Under Rendering, select the **Tasks Review** region.
    In the property editor, under Identification, enter **Milestones Review** for Title.

    ![](images/14/4_2.png)

3.	Now, you need to modify the region source query and chart attributes.
    Under Rendering, expand Regions > Milestones Review and select **Attributes**.
    In the property editor, for Appearance > Orientation, select **Vertical**.

    ![](images/14/4_3.png)

4.	Under Rendering, expand Regions > Milestones Review > Series and select **Tasks**.
In the property editor, under Identification, enter **Milestones** for Name. 
For Source > SQL Query, copy and paste the following SQL:

    ```
    select p.id
    , p.name as label
    , (select count('x') from demo_proj_milestones m 
    where p.id = m.project_id 
    and m.due_date < sysdate
    ) value
    , 'Past Milestones' series
    , p.created
    from demo_projects p
    UNION ALL
    select p.id
    , p.name as label
    , (select count('x') from demo_proj_milestones m 
    where p.id = m.project_id 
    and m.due_date >= sysdate
    ) value
    , 'Future Milestones' series
    , p.created
    from demo_projects p
    order by 5
    ```
    ![](images/14/4_4.png)

5.	Click **Save and Run Page**.

6.	The chart is displayed.
In the Developer Toolbar, click **Edit Page 10**.

    ![](images/14/4_6.png)

### HOL 14-5: Adding the Project Status Chart

In this hands-on lab, you create a pie chart to review the project completion status. You add this chart in to the Dashboard page.

1.	In the Page Designer, under Layout > Gallery, click **Regions**.
    Select **Chart** and then drag and drop to be placed underneath the Tasks Review Region.

    ![](images/14/5_1.png)

2.	In the property editor, under Identification enter the region title as **Project Status**.

    ![](images/14/5_2.png)

3.	Under Rendering, expand Series and select **New**.
    In the property editor, under Identification, enter **Status** for Name.
    Under Source, select Local Database for Location and **SQL Query** for Type.
    For Source > SQL Query, copy and paste the following SQL:
    ```
    select s.description, count(*) value
       from DEMO_PROJECTS p
       , DEMO_PROJ_STATUS s
       where p.status_cd = s.CD
       group by s.description
       order by 2 desc
    ```
    ![](images/14/5_3.png)

4.	In the property editor, under Column Mapping, select **DESCRIPTION** for Label and **VALUE** for Value.

    ![](images/14/5_4.png)

5.	Under Rendering > Project Status, select **Attributes**.
    In the property editor, for Chart > Type, select **Pie**.
    For Layout > Height, enter **250z**.

    ![](images/14/5_5.png)

6.	Under Legend, select **Yes** for Show.
    Select **End** for Position.
    Select **Rescale** for Hide and Show Behavior.

    ![](images/14/5_6.png)

7.	Under Rendering, expand Project Status > Series and select **Status**.

8.	In the property editor, for Label > Show, select **Yes**.
For Label > Position, select **Automatic**.
For Label > Display As, select **Label**.

    ![](images/14/5_8.png)

9.	Click **Save and Run Page**.

10.	The Project Status chart is now displayed in the Dashboard page.
In the Developer Toolbar, click **Application < n >**.

    ![](images/14/5_10.png)

### HOL 14-6: Adding the Project Tree

In this hands-on lab, you create the Project Tree. You create a blank page and then add the Tree region.
**Note**: You can create a Tree page by using the Create Page wizard.

1.	First, create a blank page in the Demo Projects application. In the application home page, click **Create Page**.

    ![](images/14/6_1.png)

2.	Select **Blank Page** and click **Next**.

    ![](images/14/6_2.png)

3.	Enter **16** for Page Number.
    Enter **Project Tree** for Name.
    Select **Breadcrumb** for Breadcrumb and **Reports (Page 12)** for Parent Entry.
    Click **Next**.
    
    ![](images/14/6_3.png)

4.	For Navigation Preference, select **Create a new navigation menu entry**.
    Select **Reports** for Parent Navigation Menu Entry and click **Next**.

    ![](images/14/6_4.png)

5.	On the Confirm page, click **Finish**.

6.	Now you create a Tree region. 
    In the page designer, under Rendering, right-click **Regions** and select **Create Region**.

    ![](images/14/6_6.png)

7.	In the property editor, for Identification > Title, enter **Project Tree**.
    For Identification > Type, select **Tree**.
    Under Source, select **Local Database** for Location and select **SQL Query** for Type.
    The apex-course-labs.zip file includes Project_Tree.sql file. On your local folder, navigate to the location where you unzipped the zip file and open **Project_Tree.sql**. 
    Copy the SQL code from this file and then paste it in to **Source > SQL Query** in the page designer.

    ![](images/14/6_7.png)

8.	In the page designer, navigate to Appearance and then click the **Template Options** button.

    ![](images/14/6_8.png)

9.	In the Template Options dialog:
    -	General: Select the **Remove Body Padding** check box.
    -	Header: Select **Hidden but accessible**
    -	Style: Select Remove UI Decoration
    Click **OK**.

    ![](images/14/6_9.png)

10.	In the property editor, navigate to Settings and select / enter the following: 
    -	Node Label Column: **TITLE**
    -	Node Value Column: **VALUE**
    -	Hierarchy: **Not Computed**
    -	Node Status Column: **STATUS**
    -	Hierarchy Level Column: **LEVEL**
    -	Tooltip: **Database Column**
    -	Tooltip Column: **TOOLTIP**
    Then, click **Save and Run Page**.

    ![](images/14/6_10.png)

11.	The project tree is now displayed. 

    ![](images/14/6_11.png)

12.	In the Developer Toolbar, click **Application < n >**.

    ![](images/14/last.png)












    






















