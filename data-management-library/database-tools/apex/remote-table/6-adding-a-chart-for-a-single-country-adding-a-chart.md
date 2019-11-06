# Module 6: Adding a Chart for a single Country - Adding a Chart

### **Part 1**: Creating a New Page

1. From the Runtime environment, in The Developer Toolbar (bottom of the screen), click **Application xxxxx**. 

    ![](images/6/developer-toolbar.png)

2. Click **Create Page**.  

    ![](images/6/create-page.png) 

3. For Page Type, click **Chart**, and then click **Next**. 

    ![](images/6/page-type.png)

4.  For Chart Type, click **Line**, and then click **Next**.
    ![](images/6/chart-type.png)

5. Enter the following and click **Next**.

    | Property | Enter or Select | Value |
    | --- | --- | --- |
    | Page Name | Enter | **Chart** |
    | Breadcrumb | Select | **Breadcrumb** |

    ![](images/6/naming-the-page.png)
    *Note: For, Entry Date, it automatically populates page name i.e. **Chart**.*

6. For Navigation Preference, click **Create a new navigation entry**, and then click **Next**.

    ![](images/6/navigation-preference.png)

7. For Source Type, click **SQL Query**.

8.  Enter the following sql code, and then click **Next**.
    ```
    select entry_date
    , dollar_exchange_rate
    from big_mac_index l
    where iso = 'AUS'
    order by entry_date
    ```
   ![](images/6/sql-query.png)  

9. For Label Column, select **ENTRY_DATE**. For Value Column, select **DOLLAR_EXCHANGE_RATE**, and then, click **Create**.

    ![](images/6/column-name.png)

### **Part 2**: Running the Page 

1. In Page Designer, within the Toolbar, click **Save and Run**.

    ![](images/6/save-and-run.png)

## Summary

This completes Module 6. TODO. [Click here to navigate to Module 7.](7-updating-chart-attributes-improving-the-chart.md)