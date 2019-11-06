# Module 8: Adding a Page Item and List of Values - Adding a Country List

### Information

The chart currently has the ISO code for Australia (AUS) hardcoded. By adding a select list with a list of the countries, and then modifying the chart series to utilize this page item you can easily make it easy to review the exchange rate history for any country.

To refresh the chart whenever the country in the select list is changed you need to utilize a Dynamic Action. A Dynamic Action defines client-side interactivity, and based on a specific action
(change in the select list) performs specified functions (refreshes the chart region).

In order for the chart to properly utilize the updated value in the select list, then it is necessary to submit that page item when rendering the chart.

### **Part 9.1** – Return to App Builder

- From the Runtime environment, in the Developer Toolbar (bottom of the screen), click **Edit Page 4**

![](https://i.imgur.com/ohWibTC.png[/img])

### **Part 9.2** – Add a Page Item

- From the Property Editor, in the Gallery (center pane, below Layout), click **Items**
- Click **Select List** and hold the mouse down
- Drag the item up until it is in the Items section within Chart region
- Once the Items section expands and the dark yellow box appears, release the mouse

![](https://i.imgur.com/3OaSWxj.png[/img])

### **Part 9.3** – Update the Page Item

- From the Property Editor, in the Property Editor (right pane),
update the following:
  - Identification > Name, enter **P4_COUNTRY**
  - List of Values > Type, select **SQL Query**
  - List of Values > SQL Query, enter 

  ~~~~sql
  select distinct country_name d, iso r  
  from big_mac_index  
  order by 1
  ~~~~  

   - List of Values > Display Extra Values, click **No**
   - List of Values > Null Display Value, enter - **Select Country -**

![](https://i.imgur.com/iwI2ggh.png[/img])

### **Part 9.4** – Add a Dynamic Action

- In the Rendering tree (left pane), right click on **P4_COUNTRY**, select **Create Dynamic Action**  
![](https://i.imgur.com/DqxiolP.png[/img])

- In the Property Editor (right pane), for Identification > Name, enter **Set Country** 

![](https://i.imgur.com/9YjbzLf.png[/img])
- In the Rendering tree (left pane), under Dynamic Actions > True, click **Show**
- In the Property Editor (right pane), for Identification > Action, select **Refresh**
- For Affected Elements > Selection Type, select **Region**
- For Affected Elements > Region, select **Chart**
![](https://i.imgur.com/fUoeLGJ.png[/img])

### **Part 9.5** – Update the Chart

- In the Rendering tree (left pane), under Content Body, click **Chart**
- In the Property Editor (right pane), for Source > Page Items to Submit, select **P4_COUNTRY**

![](https://i.imgur.com/nGHdsYd.png[/img])

### **Part 9.6** – Update the Chart Series

- In the Rendering tree (left pane), under Series, click **Dollar Exchange Rate**
- In the Property Editor (right pane), for Source > SQL Query, replace **'AUS'** with :**P4_COUNTRY**

![](https://i.imgur.com/UFmu3iD.png[/img])

- In the Rendering tree (left pane), under Series, click **Relative Exchange Rate**
- In the Property Editor (right pane), for Source > SQL Query, replace **'AUS'** with :**P4_COUNTRY**
- In the Rendering tree (left pane), under Series, click **Percentage Difference**
- In the Property Editor (right pane), for Source > SQL Query, replace **'AUS'** with :**P4_COUNTRY**

### **Part 9.7** – Run the Chart

- In Page Designer, within the Toolbar, click **Save and Run**
- In the Runtime environment, select different Countries

![](https://i.imgur.com/03N33qO.png[/img])

### **Learn More** *Useful Links*

- APEX Collateral http://apex.oracle.com
- Tutorials https://apex.oracle.com/en/learn/tutorials
- Community http://apex.oracle.com/community
- External Site + Slack http://apex.world