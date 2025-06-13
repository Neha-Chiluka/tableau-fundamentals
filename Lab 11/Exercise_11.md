

# 📘 Lab 11: Dynamic Dashboards and Advanced Visibility in Tableau

#### Objective:

In this lab, you will:

1. Connect Tableau to Superstore data to create detailed profit and sales visualizations.
2. Master the implementation of dynamic zone visibility to show/hide filters, legends, instructions, and entire sheets based on user interaction or parameters.
3. Explore different approaches to dashboard interactivity, including simple collapsing elements and advanced sheet swapping techniques.
4. Design dashboards that offer a tailored and intuitive user experience by controlling visibility of various components.


---

### ✅ **Report 1: Profit by State (2) Report**

1. Drag `Longitude` to the **Columns** shelf.
2. Drag `Latitude` to the **Rows** shelf.
3. Drop `State` in  **Detail** and `Profit` in **Color**
4. Drop `Category` and `Department` in **filters**.

create show sheet filter: Map in filters.

Use the below formula

`[Show Sheet]`


![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_11/1.png?raw=true)


----------



### ✅ **Report 2:Individual Item Profit and Sales Map**

1. Drag `Sales` to the **Columns** shelf.
2. Drag `Profit` to the **Rows** shelf.
3. Drop `Item` in  **Detail** 
4. Drop `Category` and `Department` in **filters**.

Drop `show sheet filter: Map` in filters.

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_11/2.png?raw=true)

---

### ✅ **Report 3: Profit by Department and Category Report**


1. Drag `Category` and `Department`  to the **Columns** shelf.
2. Drag `Profit` to the **Rows** shelf.
3. Drop `Department` in filters.

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_11/3.png?raw=true)

---

Create dashboards using the above reports experiment with hide and show tabs.

-----------------------


#### **Show/Hide Filters and Legends (Recommended: Dynamic Zone Visibility)**


**Dashboard Setup:**

1. Drag filters/legends to your dashboard. Place them in a layout container (Horizontal/Vertical) if grouping.

3. Select the filter/legend (or its container).

5. Go to the Layout tab.

7. Check "Control visibility using zones" and select your [Show Filters Trigger] calculated field.

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_11/1.1.png?raw=true)


--------------------


#### **Show/Hide Instructions (Recommended: Dynamic Zone Visibility)**

**Dashboard Setup:**

1. Drag a Text Object to your dashboard. Type your instructions into it.
2. Place this Text Object (and any other related elements) inside a layout container (Horizontal or Vertical) for better management, though a single text object can be controlled directly.
3. Select the Text Object (or its container).
4. Go to the Layout tab on the left-hand pane.
5. Check "Control visibility using zones" and select your [Show Instructions Trigger] calculated field from the dropdown.
6. Interaction:
7. Show the "Show Instructions?" parameter on the dashboard (right-click parameter > "Show Parameter").
8. Change the parameter value to toggle the visibility of the instructions.

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_11/d2.png?raw=true)


--------------------



#### **Simple Example of Collapsing**

1. Create the Dashboard:
2. Click the "New Dashboard" icon (or Dashboard > New Dashboard).
3. Set Size to "Custom (800 x 500)".
4. Drag the "Profit by Department and Category" sheet from the "Sheets" pane onto the dashboard canvas.

**Add Department Filter:**

1. Select the "Profit by Department and Category" sheet on the dashboard.
2. Click the small dropdown arrow in the top-right corner of the sheet.
3. Go to Filters and select Department. (This will add the quick filter to the dashboard).
(Optional: You can move and resize the filter on the dashboard).


![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_11/d3.png?raw=true)


--------------------


#### Sheet Swap

1.  New Dashboard is created.
3. Its Size was set to "Custom (800 x 300)".
5. Both the "Map" sheet and the "Show / Hide Filters and Legends" sheet were dragged into this same layout container.
6. The Show Sheet Parameter Control was added to the dashboard (right-click the Show Sheet parameter in the Data pane > "Show Parameter"). It's placed at the top right of the dashboard.


![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_11/d4.png?raw=true)


-----------
