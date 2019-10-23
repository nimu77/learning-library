![](images/1a.PNG)

**Oracle Application Express: Developing Database Web Applications**

**Hands-On-Labs Guide**

*Unit 11: Implementing Navigation in your Application*

In this hands-on lab, you implement navigation in the Demo Projects application. 

Breadcrumbs are very common within Web applications to allow users to easily traverse from the current page to a parent page. Use of the Back button is discouraged within Web applications, as this operation may display old ("stale") information to the user. This hands-on lab covers updating the breadcrumb entries for the following pages:
-	Demo Proj Team Members
-	Demo Projects
-	Demo Proj Milestones
-	Demo Proj Tasks

The Navigation Menu is defined as a list within Shared Components. In this hands-on lab, you update the Navigation Menu entries, and include icons for each entry.

In this hands-on lab, you update breadcrumb entries for the pages in the Demo Projects application. You also update the Navigation Menu entries and add icons for each entry.

1.	Navigate to **App Builder** and run the **Demo Projects** application.
In the navigation menu, click **Demo Proj Team Members**.
In the Developer Toolbar, click **Edit Page 2**.

2.	Update the page properties from Demo Proj Team Members to Team Members. 
In the Property Editor:
    -	Identification: Name - enter **Team Members**
    -	Identification: Title - enter **Team Members**
    Click **Save**.
    ![](images/2.png)

3.	Update the breadcrumb entry for the page. 
    a)	In the Rendering tree, click the **Shared Components** tab.
    b)	Expand the Breadcrumbs node and click the **Breadcrumb** entry.
    c)	In the Property Editor, click the **Edit Component** button.
    ![](images/3c.png)

4.	Click the **Demo Proj Team Members** breadcrumb entry.

5.	For Short Name, enter **Team Members**, and click **Apply Changes**.
    ![](images/5.png)

6.	To return to page designer, on the toolbar, click **Edit Page 2**.
    ![](images/6.png)

7.	The navigation menu is still displayed as Demo Proj Team Members. Update the Navigation Menu      entries, and include icons for each entry.
    In the page designer, click Shared Components icon in the toolbar (not the page shared components).
    ![](images/7.png)

8.	Under Shared Components, locate Navigation and click **Lists**.
    ![](images/8.png)

9.	In the Lists report, click **Desktop Navigation Menu**.
    ![](images/9.png)

10.	Click **DEMO_PROJ_TEAM_MEMBERS**.
    ![](images/10.png)

11.	On the Demo Proj Team Members list entry, locate the Image/Class item. Click at the end of the field to display a list of images. 
    ![](images/11.png)

12.	Review the library of images, provided by Font APEX. These images can be utilized throughout the application to improve aesthetics, and provide a visual indicator, rather than just text.
    Locate and select **fa-users**. 
    ![](images/12.png)

13.	For List Entry Label enter **Team Members**. 
    Click the **Next** button (>).
    ![](images/13.png)

14.	On the Demo Projects list entry, for Image/Class enter **fa-folder**, and for List Entry Label enter **Projects**. 
    Click the **Next** button (>).
    **Note**: You can simply type in the image name, such as **fa-folder**, directly into the Image/Classs field, rather than bringing up the library of images.

15.	On the Demo Proj Milestones list entry, for Image/Class enter **fa-flag**, and for List Entry     Label enter **Milestones**. 
    Click the **Next** button (>).

16.	On the Demo Proj Tasks list entry, for Image/Class enter **fa-check-square-o**, and for List   Entry Label enter **Tasks**. 
    Click the **Next** button (>).
    Click **Apply Changes**.
    ![](images/16.png)

17.	Click **Run** on the toolbar to see the updated navigation menu.
    You still need to update the icon for Dashboard.
    Navigate to Shared Components > List Details page and click Dashboard.
    ![](images/17.png)

18.	For Image/Class enter **fa-dashboard**.
    Click **Apply Changes**.

19.	Click **Run** on the toolbar to see the updated navigation menu.
    ![](images/19.png)

20.	In step 3 above, you updated the breadcrumb entry for Team Members page. Now, update the breadcrumb entries for all of the remaining pages. Perform the following steps:
    a)	In the Developer Toolbar, click **Edit Page 1**.
    b)	Click **Shared Components**.
    ![](images/20b.png)
    c)	Under Navigation, click **Breadcrumbs**.
    d)	Click **Breadcrumb**.
    e)	Now, click **Demo_Projects**.
    ![](images/20e.png)
    f)	Enter **Projects** for Short Name and click **Apply Changes**.
    g)	Then, click **Demo_Proj_Milestones**.
    h)	Enter **Milestones** for Short Name and click **Apply Changes**.
    i)	Click **Demo_Proj_Tasks**.
    j)	Enter **Tasks** for Short Name and click **Apply Changes**.

21.	Click **Run** on the toolbar.
    ![](images/21.png)

22.	Click each of the pages: Projects, Milestones and Tasks to see the updated region titles.


23.	Now, update the page properties and the breadcrumb entry for the Projects page. In the navigation menu, click **Projects**.
In the Developer Toolbar, click **Edit Page 4**.

24.	In the Property Editor:
    -	Identification: Name - enter **Projects**
    -	Identification: Title - enter **Projects** 
    Click **Save**.

25.	Now, update the page properties for the Demo Proj Milestones page. 
    In the navigation menu, click **Milestones**.
    In the Developer Toolbar, click **Edit Page 6**.

26.	In the Property Editor:
    -	Identification: Name - enter **Milestones**
    -	Identification: Title - enter **Milestones** 
    Click **Save**.

27.	Now, update the page properties and the breadcrumb entry for the Demo Proj Tasks page. In the navigation menu, click **Tasks**.
    In the Developer Toolbar, click **Edit Page 8**.

28.	In the Property Editor:
    -	Identification: Name - enter **Tasks**
    -	Identification: Title - enter **Tasks** 
     Click **Save**.

29.	Now, run the application. You need to update the Home page. Click **Edit Page 1** in the Developer Toolbar.
    ![](images/29.png)

30.	In the Page Designer, click **Page Shared Components**.
   ![](images/30.png)

31.	Under Rendering, expand **Lists** and click **Page Navigation**.
    
32.	In the Property Editor, click **Edit Component**.
    ![](images/32.png)

33.	Now, you need to edit each of the list entries. First, click **DEMO_PROJ_TEAM_MEMBERS**.
    ![](images/33.png)

34.	Replace the text in the List Entry Label with **Team Members** and click >.
    ![](images/34.png)

35.	Replace the text in the List Entry Label with **Projects** and click >.

36.	Replace the text in the List Entry Label with **Milestones** and click >.

37.	Replace the text in the List Entry Label with **Tasks** and click **Apply Changes**.

38.	Click Run Page 1 on the toolbar to see the updated Home page.
    ![](images/38.png)
    ![](images/last.png)




