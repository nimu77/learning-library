![](images/1a.PNG)

**Oracle Application Express: Developing Database Web Applications**

**Hands-On-Labs Guide**

*Unit 9: Creating Application Page Controls*


This exercise includes four hands-on-labs. The labs cover creating and updating page items, adjusting button properties, and making the form pages visually appealing. You also create and use Dynamic and Static List of Values.


**HOL 9-1 Updating the Team Members Pages**: In this hands-on lab, you update the page items on the form, and create a new collapsible sub-region to include the audit details.

**HOL 9-2 Updating the Projects Pages**: In this hands-on lab, you update the page items on the form, and create a new collapsible sub-region by copying it from another page in the application. You also create and use dynamic list of values.

**HOL 9-3 Updating the Milestones Pages**: This hands-on lab covers updating item properties, creating and using dynamic and static list of values.

**HOL 9-4 Updating the Tasks Pages**: In this hands-on lab, you create a new page item, update existing items on the form, and create a collapsible sub-region. You also use the list of values created as shared components.

### HOL 9-1 Updating the Team Members Pages

In this lab, you update the page items on the form page. You create an Audit Details collapsible sub-region on the form page. You make the form page visually appealing. This lab also covers updating the button properties and adjusting the button display on the interactive report.

1. Navigate to **App Builder** and run the **Demo Projects** application. 
   In the navigation menu, click **Demo_ Proj_ Team_ Members**. 
   In the Developer Toolbar, click **Edit Page 2**.

2. By default, buttons are positioned in the region they are associated with. Move the Create button at the top of the page to the Breadcrumbs region. In the Rendering tree, locate the CREATE button under Content Body. Click and hold the **CREATE** button and drag it up into the Breadcrumbs region.
    ![](images/1_2.png)

3. The CREATE button will appear as a child within its own Region Buttons folder.
    ![](images/1_3.png)

4. In the Property Editor:
    - Identification: Label - enter **Add Team Member**
    - Layout: Button Position - select **Create**
    - Appearance: Hot - select **Yes**
    Click **Save**. Then, click **Save and Run Page**.
    ![](images/1_4.png)

5. Navigate back to page designer. You want to view Page 3 now. In the toolbar, click the           **Navigate to next page arrow**.
    ![](images/1_5.png)

6. The generated page includes a page item for every column in the Demo_Proj_Team_Members tables. You need to make the following changes:
    - Alter the Photo Blob field to support file upload to a table
    - Since the other photo fields are populated when a file is uploaded, these items must be hidden from users
    Perform the following steps:

    a) In the Rendering tree, click the P3_PHOTO_BLOB item. For Label, enter **Photo**.
    ![](images/1_6a.png)

    b) In the Layout, hold the Ctrl key and click these items to select more than one: 
    **P3_PHOTO_FILENAME**, **P3_PHOTO_MIMETYPE**, **P3_PHOTO_CHARSET**, and **P3_PHOTO_LAST_UPDATED**.
    In the Property Editor under Identification, click the Type Quick Pick button and select **Hidden**.
    Then, click **Save**.
    ![](images/1_6b.png)

7. The tables you created earlier include audit columns for storing when and who created and last    updated each record. End users should never be allowed to enter data into these columns.          Furthermore, these columns should not display when the user creates a new record.
   Given that audit information is only reviewed occasionally, it is preferable to add these columns into a separate, collapsible region, so they can be reviewed when necessary, but do not take up excessive screen real estate the majority of time.
   Reconfigure the audit columns to be Display Only and place them in a conditional sub-region.
   In the Rendering tree, right-click **DEMO_PROJ_TEAM_MEMBER** and select **Create Sub Region**.
   ![](images/1_7.png)

8. In the Property Editor, for the New region: Identification: Title - enter **Audit Details**. 
   For Appearance>Template, select **Collapsible**.
   Click **Use Template Defaults, Expanded, Scroll-Default**.
    ![](images/1_8.png)

9. In the Template Options dialog, select **Collapsed** for Default State.
   Select **Remove UI Decoration** for Style, and click **OK**.
    ![](images/1_9.png)

10.	In the property editor, navigate to Server-side Condition. For Type, select **Item is NOT NULL**. Select **P3_ID** from the Item list.
    ![](images/1_10.png)

11.	Move the audit columns into the new region. From the Rendering tree or Grid Layout, hold the Ctrl key and click these items to select them: **P3_CREATED, P3_CREATED_BY, P3_UPDATED,** and **P3_UPDATED_BY**. 
    In the property editor, for Identification > Type, select **Display Only**.
    For Layout > Region, select **..Audit Details**.
    Click **Save**.
    ![](images/1_11.png)

12.	Page 3 is a dialog and so you cannot run it directly. Navigate to the application runtime         environment. In the navigation menu, click **Demo_Proj_Team_Members**.
    Notice the **Add Team Member** button.
    In the report, select a team member’s record to view the improved modal dialog.
    ![](images/1_12a.png)
    ![](images/1_12b.png)

### HOL 9-2 Updating the Projects Pages

In this lab, you update the page items on the form page. This lab covers creating and using List of Values. You create both static and dynamic list of values. You create an Audit Details collapsible sub-region on the form page.

1.  In the application runtime environment, click **Demo_Projects**.
   Then, in the Developer toolbar, click **Edit Page 4**.

2.  The Project Lead column is currently displaying an identifier instead of the team member's        name. Defining a List of Values within Shared Components enables the same control to be used      on this page and also the form page for projects.
   In Page Designer, click the **Shared Components** button, found on the right side of the toolbar (not in the Rendering tree).
    ![](images/2_2.png)

3.  Under Other Components, click **List of Values**. 
    ![](images/2_3.png)

4.  Then, click **Create**.

5.  For Create List of Values, select **From Scratch** and click **Next**.

6.  Enter **Team Members** for Name, select **Dynamic** for Type, and click **Next**.
    ![](images/2_6.png)

7.  For Query, replace the existing SQL with the following and click **Create List of Values**.

    ```
	select full_name as display,
	id as return 
	from demo_proj_team_members   
	order by 1  
    ```   
    ![](images/2_7.png)

8. Click **Edit Page 4** on the toolbar, to return to Page Designer.
    ![](images/2_8.png)

9.  In the Rendering tree, expand the **Columns** node under the DEMO_PROJECTS region.
    Click the **PROJECT_LEAD** column.

10. In the property editor:
    -	Identification > Type: select **Plain Text (based on List of Values)**
    -	List of Values: select **Team Members**
    -	Heading > Alignment: select **Start**
    -	Layout > Column Alignment: select **Start**
    Click **Save**.
    ![](images/2_10.png)

11. It would look more aesthetically pleasing to place the Create button at the top of the page.
    In the Layout, locate the Breadcrumbs region. Note that there are several elements surrounded by dotted lines. These are placeholders for buttons.
    Locate the **DEMO_PROJECTS** region. Click and hold the **Create** button and drag it up to the Breadcrumbs region and into the Create placeholder.
    ![](images/2_11.png)

12. In the property editor, enter **Create Project** for label.
    Under Appearance, select **Yes** for Hot.
    ![](images/2_12.png)

13. Click **Save**. Then, click **Save and Run Page**.

14. Your screen might look like:
    ![](images/2_14.png)

15. You need to update page items on the Maintain Project form page. Click a project name and then in the Developer Toolbar, click **Edit Page 5**.

16.	In the Layout, under Content Body, click the P5_PROJECT_LEAD item. In the Property Editor:
    - Identification: Type– select **Select List**
    - List of Values: Type – select **Shared Component**
    - List of Values: List of Values – select **Team Members**
    - List of Values: Display Extra Values – select **No**
    - List of Values: Display Null Value – select **Yes**
    - List of Values: Null Display Value – enter **–Select Team Member-**
    ![](images/2_16.png)

17.	Next define a list of statuses. In Page Designer, click the **Shared Components** button, found on the right side of the toolbar. Perform the following steps:
    a)	Under Other Components, click **List of Values**.
    b)	For Create List of Values, select **From Scratch** and click **Next**.
    c)	Enter Statuses for Name, select **Dynamic** for Type, and click **Next**.
    d)	For Query, replace the existing SQL with the following and click **Create List of Values**.
    ```
    select description as display,
    cd as return
    from demo_proj_status
    order by 1
    ```
    e)	Click Edit Page 4 on the toolbar, to return to Page Designer.

18.	Navigate to the Demo Projects application runtime environment. 
    In the navigation menu, click **Demo Projects**. 
    Click a project name. Click a project name and then in the Developer Toolbar, click **Edit Page 5**.
    In the Layout, under Content Body, click the **P5_STATUS_CD** item. In the Property Editor:
    -	Identification: Type– select **Select List**
    -	List of Values: Type – select **Shared Component**
    -	List of Values: List of Values – select **Statuses**
    -	List of Values: Display Extra Values – select **No**
    -	List of Values: Display Null Value – select **Yes**
    -	List of Values: Null Display Value – enter **–Select Status-**
    ![](images/2_18.png)

19.	Click the **P5_COMPLETED_DATE** item. 
    In the property editor, under Appearance, select **Required - Floating** for Template. 
    Then, click **Save**.
    ![](images/2_19.png)

20.	In the lab HOL 9-1, you created a sub-region called Audit Details for the Maintain Team           Member page (Page 3). Since the four items included in that region are the same as those on       the Maintain Project page and are associated with the exact same database columns, you can        copy them to the Maintain Project page. This approach is easier than creating a new region        and updating the items. Copying the region will also copy the previously defined template and     template options. 
    Delete the four audit items before copying the Audit Details region to this page. If you do not delete them, the item names in the copied Audit Details region will be renamed with a unique name (for example, P5_CREATED will be renamed to P5_CREATED_1) to ensure all page items have unique names. Although this renaming will not break the page processing, Oracle does not recommend this approach.
    In the Layout, hold the Ctrl key and select the items: **P5_CREATED, P5_CREATED_BY, P5_UPDATED**, and **P5_UPDATED_BY**.
    Then, right-click and select **Delete**.
    Click **Save**.
    ![](images/2_20a.png)

21.	In page designer, navigate to **Page 3**.

22.	In the Rendering tree, right-click the **Audit Details** sub region and select **Copy to other Page....**
    ![](images/2_22.png)

23.	Enter 5 for To Page and select **Yes** for Copy Region Items. Click **Next**.
    ![](images/2_23.png)

24.	Click **Copy**.

25.	In Page Designer, navigate back to **Page 5**.

26.	In the Rendering tree, select the **Audit Details** sub region. 
In the Property Editor, for Layout: Parent Region select **Demo Project**.
    ![](images/2_26.png)

27.	In the Layout, hold the Ctrl key and select the items: **P5_CREATED, P5_CREATED_BY, P5_UPDATED,** and **P5_UPDATED_BY**.
    In the property editor, under Source, for Form Region, select **Demo Project**.
    Click **Save**.

28.	Now, reposition the buttons. Under Rendering > Buttons > Region Buttons, select **CANCEL**.       In the property editor, for Layout: Button Position select **Previous**. 
    Click **Save**.
    ![](images/2_28.png)

29.	Navigate to the Demo Projects application runtime environment. 
    In the navigation menu, click **Demo Projects**. 
    Click a project name. Notice the modified dialog. Expand the Audit Details node.
    ![](images/2_29.png)

### HOL 9-3 Updating the Milestones Pages

In this lab, you update the page items on the form page. You create the Audit Details collapsible sub-region by copying it from another page in the application. You make the form page visually appealing. This lab also covers creating and using list of values.

1.  In the Demo Projects application runtime environment, click **Demo Proj Milestones** in the navigation menu.
    In the Developer Toolbar, click **Edit Page 6**.

2.  The Project Id column is currently displaying an identifier instead of the project name. Defining a List of Values within Shared Components enables the same control to be used on this page, the form page for milestones, and the task pages.
    In Page Designer, click **Shared Components** found on the right on the toolbar.

3.  Under Other Components, click **List of Values**.

4.  Click **Copy**.
    ![](images/3_4.png)

5.  Select **Team Members-Dynamic** from Copy List of Values.
    Enter **Projects** for New List of Values Name.
    Click **Copy**.
    ![](images/3_5.png)

6.  Click the **Projects** List of Values entry.

7.  For Query, replace the existing SQL with the following.
    ```
    select name as display
    , id as return
    from demo_projects
    order by 1
    ```
    Click **Apply Changes**.

8.  Click **Edit Page 6** on the toolbar, to return to Page Designer.
    ![](images/3_8.png)

9.  In the Rendering tree, expand the Columns node under the DEMO_PROJ_MILESTONES region.
    Select the **PROJECT_ID** column.
    In the Property Editor:
    - Identification: Type - select **Plain Text (based on List of Values)**
    - List of Values: List of Values - select **PROJECTS**
    - Heading: Heading - enter **Project**
    - Layout: Column Alignment - select **start**
    ![](images/3_9.png)

10.	The Name column is ambiguous and should be relabeled.
In the Rendering tree, click the Name column.
In the Property Editor, for Heading enter **Milestone**.

11.	Reposition the CREATE button to the top of the page. 
Locate the **DEMO_PROJ_MILESTONES** region and select the **Create** button.

12.	In the Property Editor:
    - Identification: Label - enter **Create Milestone**
    - Layout: Region - select **Breadcrumb**
    - Layout: Button Position - select **Create**
    - Appearance: Hot - select **Yes**
    ![](images/3_12.png)

13.	Click **Save**. Then, click **Save and Run Page**.
    ![](images/3_13.png)

14.	Click a project name. In the Developer Toolbar, click **Edit Page 7**.

15.	Update the page items. Under Rendering, expand Items, select the **P7_PROJECT_ID** item. In the Property Editor:
    -	Identification: Type - select **Select List**
    -	Label: Label - enter **Project**
    -	List of Values: Type - select **Shared Component**
    -	List of Values: List of Values - select **PROJECTS**
    -	List of Values: Display Extra Values - select **No**
    -	List of Values: Null Display Value - enter **- Select Project –**
    ![](images/3_15.png)

16.	In the Rendering tree, select the P7_NAME item. In the Property Editor:
    - Label: Label - enter Milestone

17.	Delete the four audit items from the Maintain Milestone page. Under Rendering, hold the Ctrl      key and select the items: **P7_CREATED, P7_CREATED_BY, P7_UPDATED,** and **P7_UPDATED_BY**.
    Then, right-click and select **Delete**.
    Click **Save**.

18.	Copy the Audit Details region from Page 3 to Page 7. In page designer, navigate to **Page 3**.

19.	In the Rendering tree, right-click the **Audit Details** sub region and select **Copy to other Page....**
    ![](images/3_19.png)

20.	Enter 7 for To Page and select **Yes** for Copy Region Items. Click **Next**.

21.	Click **Copy**.

22.	In Page Designer, navigate back to **Page 7**.

23.	In the Rendering tree, select the **Audit Details** sub region. In the Property Editor, for Layout: Parent Region select **Demo Proj Milestone**.
    ![](images/3_23.png)

24.	In the Layout, hold the Ctrl key and select the items: **P5_CREATED, P5_CREATED_BY, P5_UPDATED,** and **P5_UPDATED_BY**.
    In the property editor, under Source, for Form Region, select **Demo Proj Milestone**.
    Click **Save**.

25.	Now, reposition the buttons. Under Rendering > Buttons > Region Buttons, select **CANCEL**.       In the property editor, for Layout: Button Position select **Previous**.

26.	Click **Save**. 
    Navigate to the application runtime environment and click **Demo_Proj_Milestones**.
    Click any milestone to see the modified dialog.
    ![](images/3_26.png)

### HOL 9-4 Updating the Tasks Pages

In this lab, you update the page items on the form page. You use list of values created as shared components. This lab also covers creating a new page item on the form page. You make the form page visually appealing. 

1.	In the Demo Projects application runtime environment, click **Demo_Proj_Tasks** in the navigation menu.
    In the Developer Toolbar, click **Edit Page 8**.

2.	The Project Id, Milestone Id, and Assignee columns are currently displaying identifiers           instead of the names. You already created a List of Values for projects and assignees (Team       Members). Therefore, you only need to create a List of Values for milestones.
    In Page Designer, click **Shared Components** found on the right on the toolbar.

3.	Under Other Components, click **List of Values**.

4.	Click **Copy**. 
    ![](images/4_4.png)

5.	Select **Projects-Dynamic** from Copy List of Values.
    Enter **Milestones** for New List of Values Name.
    Click **Copy**.

6.	Click the **Milestones** List of Values entry.

7.	For Query, replace the existing SQL with the following. 
    ```
    select name as display
    , id as return
    from demo_proj_milestones
    order by 1
    ```
    Click **Apply Changes**

8.	Click Edit Page 8 on the toolbar, to return to Page Designer.

9.	In the Rendering tree, locate the DEMO_PROJ_TASKS region. Expand the Columns node, and click the **ASSIGNEE** column. In the Property Editor:
    -	Identification: Type - select **Plain Text (based on List of Values)**
    -	List of Values: List of Values - select **TEAM MEMBERS**
    -	Layout: Column Alignment - select **start**
    ![](images/4_9.png)

10.	In the Rendering tree, click the **PROJECT_ID** column. In the Property Editor:
    -	Identification: Type - select **Plain Text (based on List of Values)**
    -	List of Values: List of Values - select **PROJECTS**
    -	Heading: Heading - enter **Project**
    -	Layout: Column Alignment - select **start**

11.	In the Rendering tree, click the **MILESTONE_ID** column. In the Property Editor:
    -	Identification: Type - select **Plain Text (based on List of Values)**
    -	List of Values: List of Values - select **MILESTONES**
    -	Heading: Heading - enter **Milestone**
    -	Layout: Column Alignment - select **start**

12.	The Name column is ambiguous and should be relabeled. In the Rendering tree, click the **NAME** column. 
    In the Property Editor, for Heading enter **Task**.

13.	The IS_COMPLETE_YN column should be relabeled and the values should be Yes / No, rather than      Y / N. To change the displayed value, you can either modify the SQL Source for the report, or     define a List of Values. 
    In the Rendering tree, select the **Demo Proj** Tasks region.
    In the Property Editor, for Source > Type, select **SQL Query**.

14.	For the SQL Query, replace "IS_COMPLETE_YN", with the following:
    ```
    decode (IS_COMPLETE_YN, 'Y', 'Yes', 'No') as "IS_COMPLETE_YN",
    ```
    ![](images/4_14.png)

15.	In the Rendering tree, click the **IS_COMPLETE_YN** column. 
    In the Property Editor, for Heading enter **Completed?**

16.	Reposition the CREATE button to the top of the page. Locate the **Demo Proj Tasks** region. 
    Select the **Create** button. 
    In the Property Editor:
    -	Identification: Label - enter **Create Task**
    -	Layout: Region - select **Breadcrumb**
    -	Layout: Button Position - select **Create**
    -	Appearance: Hot - select **Yes**
    ![](images/4_16.png)

17.	Click **Save**. Then, click **Save and Run Page**.

18.	In the interactive report, rearrange the Task and Assignee columns so that Task is displayed first followed by Assignee.
    Click **Actions > Columns**.
    In the Select Columns dialog, select **Task**, click the **Up** button once and then click **Apply**.
    ![](images/4_18.png)

19.	Then, click **Actions > Report > Save Report**. 
    For Save, select **As Default Report Settings**. 
    For Default Report Type, select **Primary** and click **Apply**. 
    The default report is saved for all users.
    Your screen should look like:
    ![](images/4_19.png)

20.	In the interactive report, click a task. Then, in the Developer Toolbar, click **Edit Page 9**.

21.	Update the page items. The first requirement is to shuffle the page items, using drag and drop in either the Rendering tree or the Layout, such that the items are in the following order:
    -	P9_PROJECT_ID
    -	P9_MILESTONE_ID
    -	P9_NAME
    -	P9_DESCRIPTION
    -	P9_ASSIGNEE
    -	P9_START_DATE
    -	P9_END_DATE
    -	P9_IS_COMPLETE_YN
    ![](images/4_21.png)

22.	Under Rendering, select the **P9_PROJECT_ID** item. In the Property Editor:
    -	Identification: Type - select **Select List**
    -	Label: Label - enter **Project**
    -	List of Values: Type - select **Shared Component**
    -	List of Values: List of Values - select **PROJECTS**
    -	List of Values: Display Extra Values - select **No**
    -	List of Values: Null Display Value - enter **- Select Project –**

23.	The Milestones item should be defined as a Cascading List of Values, whereby only the milestones for the currently selected Project item are displayed. In the Layout, under Content Body, click the **P9_MILESTONE_ID** item. In the Property Editor:
    -	Identification: Type - select **Select List**
    -	Label: Label - enter **Milestone**
    -	List of Values: Type - select **SQL Query**
    -	List of Values: SQL Query - copy and paste the following:
    ```
    select name as display, id as return
    from demo_proj_milestones
    where project_id = :P9_PROJECT_ID
    order by 1
    ```
    -	List of Values: Display Extra Values - select **No**
    -	List of Values: Null Display Value - enter **- Select Milestone -**
    -	List of Values: Cascading LOV Parent Item(s) - select **P9_PROJECT_ID**
    **Note**: You cannot use the MILESTONES List of Values for this item, as this query needs to limit the milestone records returned to those for the selected project, using P9_PROJECT_ID.
    ![](images/4_23.png)

24.	In the Rendering tree, click the **P9_NAME** item. In the Property Editor:
    -	Label: Label - enter **Task**

25.	In the Grid Layout, under Content Body, click the **P9_ASSIGNEE** item. In the Property Editor:
    -	Identification: Type - select **Select List**
    -	List of Values: Type - select **Shared Component**
    -	List of Values: List of Values - select **TEAM_MEMBERS**
    -	List of Values: Display Extra Values - select **No**
    -	List of Values: Null Display Value - enter **- Select Assignee –**

26.	In the Rendering tree, click the **P9_IS_COMPLETE_YN** item. In the Property Editor:
    -	Identification: Type - select **Switch**
    -	Label: Label - enter **Completed?**
    ![](images/4_26.png)

27.	Delete the four audit items from the Maintain Milestone page. In the Rendering tree, hold the     Ctrl key and click these to select them all: **P9_CREATED, P9_CREATED_BY, P9_UPDATED,** and       **P9_UPDATED_BY**. 
    Then, right-click and select **Delete**.

28.	Click **Save**.

27.	Copy the Audit Details region from Page 3 to Page 9. In page designer, navigate to **Page 3**.

28.	In the Rendering tree, right-click the **Audit Details** sub region and select **Copy to other Page....**

29.	Enter **9** for To Page and select **Yes** for Copy Region Items. Click **Next**.

30.	Click **Copy**.

31.	In Page Designer, navigate back to **Page 9**.

32.	In the Rendering tree, select the **Audit Details** sub region. 
    In the Property Editor, for Parent Region select **Demo Proj Task**. 
    Click **Save**.

33.	In the Layout, hold the Ctrl key and select the items: **P5_CREATED, P5_CREATED_BY, P5_UPDATED,** and **P5_UPDATED_BY**.
    In the property editor, under Source, for Form Region, select **Demo Proj Task**.
    Click **Save**.

34.	Navigate to the application runtime environment and click **Demo_Proj_Tasks**.
    Click any project to see the modified dialog.
    ![](images/4_34.png)

35.	Click **Edit Page 9** in the Develop Toolbar, to return to Page Designer.

36.	It would also be beneficial to include the Milestone Due Date on the page so it can be compared to the Task End Date. To facilitate this add a display only item and then populate the item based on the selected Milestone.
In the Layout, click the bottom divider to display the Gallery. In the Gallery, click **Items** and locate **Display Only**.
    ![](images/4_36.png)

37.	Click and hold **Display Only** and drag it to the left of the **P9_MILESTONE_ID** in the Layout.
    You will need to hover to the left of the existing item before the dark yellow box displays next to the existing item.
    ![](images/4_37.png)

38.	Set the attributes for the new item. In the Property Editor:
    -	Identification: Name - enter **P9_MILESTONE_DUE_DATE**
    -	Label: Label - enter **Due Date**
    -	Source: Type - select **Null**
    - 	Source: Maintain Session State - select **Per Session**

    **Note**: This item is display only and is not based on a Database Column. As such it is very important to not save session state for this item and to set the source type appropriately.
    ![](images/4_38.png)
    ![](images/last.png)










