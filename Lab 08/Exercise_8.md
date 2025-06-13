# 📘 Lab 8: Building Interactive Dashboards and Advanced Actions

#### Objective:

In this lab, you will:

1. Connect Tableau to Superstore data to conduct comprehensive profit and sales analysis.
2. Develop multi-layered interactive dashboards, including those optimized for different device types (e.g., phone).
3. Implement and understand various dashboard actions such as filter actions, set actions, and highlight actions.
4. Utilize sets (simple and combined) to drive dynamic interactions and analysis.
5. Create Key Performance Indicators (KPIs) and integrate them into scorecards for regional performance evaluation.
6. Master techniques for blending different report types within a single dashboard to provide a holistic view.

---

### ✅ **Report 1: Overall Profit by Category Report**

1. Drag **Profit** to the Columns shelf.
2. Drop **Category** in Rows 
3. Create a Set for Item and name it as Action(Item).

Drop this in Filters


![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_8/1.png?raw=true)

---

### ✅ **Report 2: Top 10 Least Profitable Items**


**Steps**:


1. Drag **Profit** to the **Columns** shelf.
2. Drop **Item** in **Rows** 
3. Create a **Set** for `Category` and name it as** Action(Category)**. (Drop in Filters)
4. Drop `Item` in **Filters** and use the below configuration

5. Drop `Action(Category)` and set it to **Show In/Out Set**

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_8/2.png?raw=true)

---

### ✅ **Report 3: Profit by State Report**


1. Drag **Longitutde** to the **Columns** shelf.
2. Drop **Latitude** in **Rows** 

3. Drop `Action(Category)` and `Action(Item)` in **filters**
4. Drop `Profit` in **Color** and `State` in **Detail**

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_8/3.png?raw=true)

----

### ✅ **Report 4: Profit Trend Report**


1. Drag **Order Date** to the **Columns** shelf. ( Set it to Quarter)
2. Drop **Profit** in **Rows** 

3. Drop `Action(Category)` and `Action(Item)` in **filters**
4. Right click on the graph and add a trend line and check the boxes for Show confidence bands

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_8/4.png?raw=true)

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_8/4.2.png?raw=true)

-----

### ✅ Dasboard 1 : Is Least Profitable Always Unprofitable? 

1. Click on Dashboard from the Title Pane and create new dashboard. 
2. Select the 4 reports that we have created so far. Name the sheet as `Is Least Profitable Always Unprofitable`
3. Add a filter for Department. You can find the filter on the Objects option on the data pane. 

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_8/d1.png?raw=true)

--------

### ✅ **Dasboard 2 : Profit Analysis (Different Devices)**

Just duplicate Report 1 
Rename it and change the device type to Phone. 
![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_8/d2.png?raw=true)

-----

### ✅ **Report 5: Source**

1. Drag **Sales** to the Columns shelf. 
2. Drop **Category** in Rows 

Sort the axis to desending order.

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_8/5.png?raw=true)

 -----
 ### ✅ **Report 6: Target**

1. Drop  `Order Date` in Columns(Set as Quarter)
2. Drop `Sales` in Rows
3. Drop `Action(Category)` to **Filters** and choose only **Tables**

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_8/6.png?raw=true)

---------

### ✅ **dasboard 3: Source and Target Example **

1. Create a **dashboard**.
2. Click on **Dashboard** from the Title Pane and create new dashboard. 
3. Choose the **Source** and **Target** reports

> Trigger a filter action by clicking one or more Category bars.
Then navigate to the Target sheet to see the filter that Tableau applies.

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_8/d3.png?raw=true)

------------
### ✅ **Report 7 : Source**

Similar to the previous dashboard we will be creating a new one.

1. Drag **Region** to the Columns shelf. 
2. Drop **Category** in Rows 

3. Drop `Sales` in **Color** and **Label**

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_8/7.png?raw=true)

---
### ✅ **Report 8  :Target **

1. Drop  `Order Date` in Columns(Set as Quarter)
2. Drop `Sales` in Rows
3. Ceate a combined set for Action(Category, Region). Just Press CRTL and choose both the fields. Then right click and choose combine fields.


Drop this combined field to **Filters** and choose only **Office Machines, West.**


![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_8/8.png?raw=true)

---

### ✅ dasboard 4: Source and Target (with multiple dimensions) 

Create a **Dashboard** and add the newly created **Source** and **Target** reports.

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_8/d4.png?raw=true)

------------
### ✅ **Report 9  :Regions **

1. Drop  `Longitude` in **Columns**
2. Drop `Latitude` in **Rows**
3. Drop 'Region' in **Color** and `State` in **Detail**.

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_8/9.png?raw=true)

---------
### ✅ Report 10  :Sales and Profit by State 

1. Drop  `Profit` in **Columns**
2. Drop `Sales` in **Rows**
3. Drop 'Region' in **Color** and `State` in **Detail**.

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_8/10.png?raw=true)

------------

### ✅ Report 11  : Sales by Region

1. Drop  `Sales` in **Columns**
2. Drop `Region` in **Rows**
3. Drop 'Region' in **Color** 

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_8/11.png?raw=true)

-----------------------

### ✅ dasboard 5: Highlighting Example

Create a Dashboard and add the newly created Sales by Region , Regions and Sales and Profit by State  reports. You can also add a filter for Highlighting a state. 

> Select any mark in any view to highlight by Region.
Use the Highlighter for State to highlight matching states.

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_8/d5.png?raw=true)

---------

### ✅ Report 12  : Sales by Region  (set actions)

1. Drop  `Longitude` in Columns
2. Drop `Latitude` in Rows
3. Drop `Region` in **Color** and in **Detail**.
4. Drop `Sales` in **Detail**.

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_8/12.png?raw=true)

---------------
### ✅ Report 13  :Sales by Category (set actions)
1. Drop  `Sales` in **Columns**
2. Drop `Category` in **Rows**
3. Create a **Set** for `Region`. Choose Central for the visualization. And set In/Out and choose In.
Drop '**Region**' in **Color**

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_8/13.png?raw=true)

----------
### ✅ dasboard 6: Sales by Region and Category (set actions).

Create a **Dashboard** and add the newly created `Sales by Region  (set actions)` and `Sales by Category (set actions)`

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_8/d6.png?raw=true)

------------------

### ✅ Report 14  :Region Scorecard

1. Drop  `Order Date` in Columns. Set it to Month
2. Drop `Region` in Rows
3.  Drop Order Date in Filters and set custom Date format as Month/Year
4. Create a calculated field KPI - Profit Ratio and add the below formula

```python
IF [Profit Ratio] >= [Profit Ratio KPI Target]
THEN "Acceptable"
ELSE "Poor"
END


```

5. Under **Marks** card change the type to **Shape**. And drop **KPI** in **Shape** and **Color**.

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_8/14.png?raw=true)


----------------

### ✅ Report 15  :Region Scorecard

1. Drop  `Longitude` in Columns
2. Drop `Latitude` in Rows
3. Drop `KPI - Profit Ratio` in **Color** and **Text**
4. Drop `Region` in **Label** and **Detail**

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_8/15.png?raw=true)

----------

### ✅ dasboard 7: Regional Scorecard (last 6 months).

Create a **Dashboard** and add the newly created reports and set the **Device type** to **Phone**

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_8/d7.png?raw=true)

-----

### ✅ Report 16  : Profit Ratio KPI by State

1. Drop  `Longitude` in Columns
2. Drop `Latitude` in Rows
3. Drop '`KPI - Profit Ratio` ' in **Color** and **Detail**
4. Drop `State` in **Detail**.
5. Drop `Region` in **Filters** and choose **South**.

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_8/16.png?raw=true)


------------

### ✅ Report 17  : Profit Ratio by Quarter

1. Drop  `Order Date` in Columns. Set to Quarter
2. Drop `KPI - Profit Ratio` in Rows. 
3. Drop `Region` to `South`
4. Drop `Action (State)` to Filters 

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_8/17.png?raw=true)

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_8/17.2.png?raw=true)

------

### ✅ dasboard 8: Profit Ratio Analysis.

Create a Dashboard and add the newly created reports.

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_8/d8.png?raw=true)

----------

### ✅ dasboard 9: South Region Analysis.



Create a Dashboard and add the Profit Ratio Analysis. Add Caption Boxes and filters for Region. 


![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_8/d9.png?raw=true)
