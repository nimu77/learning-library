# Module 5: Updating the Report in the Runtime environment - Updating the Report View

### **Part 1**: Resequencing the columns

1. In the Runtime environment, click **Actions**, and then click **Columns**.

    ![](images/5/click-action-column.png)

2. Select **Entry Date**, click **Top** icon, and then click **Apply**.  
    ![](images/5/entry-date.png)

### **Part 2**: Sorting the Records

1. Click **Actions**, select **Data**, and then click **Sort**.
    ![](images/5/sorting-data.png)
2. **1 - for Column** select **Entry Date**, and for **Direction** select **Descending**. **2 - for Column** select **Country Name**, and then click **Apply**.  
    ![](images/5/sorting-column.png)

### **Part 3**: Adding a Computation

1. Click **Actions**, select **Data**, and then click **Compute**.

    ![](images/5/selecting-compute.png)

2. Enter the following and then click **Apply**.

    | Property | Enter or Select | Value |
    | --- | --- | --- |
    | Column Name | Enter | **Difference%** |
    | Format Mask | Select | **5,234.10** |
    | Computation Expression | Enter | **(K – F) * 100 / F** |

    ![](images/5/new-computation.png)  
    *Note: **K** references Relative Exchange Rate and **F** references Dollar Exchange Rate as listed under Columns*

### **Part 4**: Saving the Report

1. Click **Actions**, select **Report**, and then click **Save Report**.  
    ![](images/5/save-report.png) 
2. For Save, select **As Default Report Settings**. (This option is only available to Developers). 
    ![](images/5/as-default-report-settings.png)  
3. For Default Report Type, select **Primary**, and then click **Apply**. 
    ![](images/5/select-primary.png)

## Summary

This completes Module 5. TODO. [Click here to navigate to Module 6.](6-adding-a-chart-for-a-single-country-adding-a-chart.md)