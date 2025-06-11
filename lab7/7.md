# 📘 Lab 7: Advanced Data Visualization and Formatting in Tableau

#### Objective:

In this lab, you will:

1. Connect Tableau to Superstore data to analyze sales and profit across various dimensions.
2. Master techniques for handling and visualizing missing data points using different formatting options.
3. Enhance reports with trend lines, confidence bands, and annotations for deeper insights.
4. Apply dramatic and detailed formatting to improve visual impact and readability.
5. Customize tooltips for richer interactive experiences.
6. Learn to create and utilize Sets, including combined sets, for flexible data analysis and filtering.

---

### ✅ **Report 1: Sales by Department and Category Report**

1. Drag **Customer Segment** to the Columns shelf.
2. Drop **Department** and **Category** in Rows 
3. Drop Sales in Text

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_7/1.png?raw=true)


---

### ✅ **Report 2: Custom Date Formatting**


**Steps**:


1. Drop `Order Date`( set it as Month) in **Columns**
2. Drop `Sales` in **Rows**. 
3. Drop `Order Date`  in **Filters** ( Choose Year 2016)

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_7/2.png?raw=true)

---

### ✅ **Report 3: Show at Indicator Report**


1. Drop `Order Date`( set it as Day) in **Columns**
2.Ceate Calculated field `Profit (some nulll values)`

**Formula**

`IF INT([Profit]) % 5 != 0 THEN [Profit] END`

Drop this field in **Rows**. 
3. Drop `Order Date` in Filters ( Choose Year 2016)
4. Add `Order Date` in Filters and choose December 2016
5. Add Department -> Furniture in Filters

6. Now add a reference line using the below configuration

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_7/3.png?raw=true)

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_7/3.2.png?raw=true)

----

### ✅ **Report 4: Show at Default Value Report**

Duplicate the report 3 

1. Right click on the left axis -> Format ->Pane-> Special Values -> Show at Default Value

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_7/4.png?raw=true)

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_7/4.2.png?raw=true)

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_7/4.3.png?raw=true)

-----

### ✅ **Report 5: Hide (Connect Lines) Report**

Duplicate the report 4

1. Right click on the left axis -> Format ->Pane-> Special Values -> Hide (Connect Lines)

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_7/5.png?raw=true) 

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_7/5.2.png?raw=true)

--------

### ✅ **Report 6: Hide (Break Lines) Report**

Just duplicate Report 5. 


1. Right click on the left axis -> Format ->Pane-> Special Values -> Hide (Break Lines)

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_7/6.png?raw=true)

-----

### ✅ **Report 7: Bar Chart indicates missing days**



1. Just Replace `Profit` instead of `Profit (some nulll values)` in rows
2. In **Marks** card set the type of visual to **Bar**

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_7/7.png?raw=true)

 -----
 ### ✅ **Report 8: Sales Trends Report**

1. Drop `Department` and `Order Date` in **Columns**(Set as Quarter)
2. Drop `Sales` in **Rows**
3. Drop `Department` in **Filters** (Set as Office Suplies)
4. `Order Date` in **filters** (Set to Quarters) again click on the arrow to set Year/Quarter format
5. Right click on the graph and select show trend lines
6. Right click on the trend line -> Edit all Trend Lines -> Check the box of Show confidence brands. 
7. Now select a point in the lowest drop and right click -> Annotate -> set a configuration like below
Similarly you can do this for highest point in the graph as well.

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_7/8.png?raw=true)

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_7/8.2.png?raw=true)

---------

### ✅ **Report 9: Dramatic Formatting Report**

1. Drop `Order Date` in Columns set as  **Quarter**
2. Drop `Sales` in Rows. 
3. Drop `Department` in Filters (Set as Office Suplies)
4.  `Order Date` in filters (Set to Quarters) again click on the arrow to set Year/Quarter format
5. Right click on the left axis -> format -> Axis -> Font(Blue) and Title (Blue)-> Under **Scale** set **Numbers** to 2 decimal  and change the currency to $.
6. Click on the Shading and Set Worksheet Color to Black.
7. Add the trend line and annotations to highest and lowest points of the graph.

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_7/9.png?raw=true)

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_7/9.2.png?raw=true)

------------
### ✅ **Report 10 : Exploring Tooltips Report**

Duplicate the above report 9

1. Drop `Department` again to **Filters** and choose **Use all**
2. Drop `Department` into **Detail** and **Tooltips**
3. Change the Worksheet color to white using formating.

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_7/10.png?raw=true)

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_7/10.2.png?raw=true)

---

### ✅ **Report 11 : Sales by Categories Report**


1.Drop `Sales` in **Columns**. 
2. Drop `Category` to **Rows**
3.Do some formatting using by clicking on the left axis (set the currency and units)
4. Create a **Set** for `Department`:

- Right-click Department in the data pane.

- Select Create → Set

- Name it: Department Set

- Choose “All” or specific values → Click OK

5. Create a Set for Order Date by Quarter:

- Right-click Order Date → choose Create → Custom Date

- Set to: Quarter

- Name it: Order Date (Quarter)

- Then right-click Order Date (Quarter) → choose Create → Set

- Name it: Quarter Set

- Select values (or all) → Click OK

6. Create a Combined Set:

- Ctrl+select Department Set and Quarter Set in the data pane.

- Right-click → choose Create Combined Set

`Tooltip (Department,QUARTER(Order Date))`

Click OK

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_7/11.png?raw=true)

---
