
# 📘 Lab 6: Mastering Table Calculations in Tableau

#### Objective:

In this lab, you will:

1. Connect Tableau to sales data.
2. Explore and apply various quick table calculations, including running sums and year-over-year growth.
3. Understand and configure addressing and partitioning for table calculations.
4. Utilize a range of advanced table calculation functions such as INDEX(), First(), Last(), Size(), LOOKUP(), Previous_Value(), RUNNING_MIN(), RUNNING_SUM(), WINDOW_MAX(), WINDOW_SUM(), RANK(), and TOTAL().
5. Analyze sales performance across different dimensions using these powerful calculation techniques.

---

### ✅ **Report 1: Quick Table Calc - Running Sum Report**

1. Drag **Order Date** to the Columns shelf.(set to Month)
2. Drop **Sales** in Rows Twice. For the second Sum(Sales)create a table calculation as follows

3. Create a refernce line for Orders axis. Use the configuration as below


Double tap in sheet 1 and rename it as **Quick Table Calc - Running Sum Report**

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_6/1.png?raw=true)
![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_6/1.2.png?raw=true)

---

### ✅ **Report 2: Sales by Region and Department**


**Steps**:

Duplicate the report 1. 

1. Drop `Region` and `Department` in **Columns**
2. Drop `Order date` twice in **Rows**. Change them to **Year** and **Quarter** respectively.
3. Drop `Region (East & West)` and `Order Date(Year)` in Filter
3. Drop `Sales` in **Text**

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_6/2.png?raw=true)

---

### ✅ **Report 3: Addressing and Partitioning Report**

**Duplicate report 2**

1. Create a calculated field under **Tables**. Name the field as **Index** and enter the below formula.

**Formula**

`INDEX()`

Drop this in Text 

2. Do a table calculation to the INDEX() as below:


![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_6/3.png?raw=true)

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_6/3.2.png?raw=true)


----

### ✅ **Report 4: Meta Table Calculations Report**

1. Drop `Measure Names` in Columns
2. Drop `Department` and `Category` in Rows
3. Create Calculated fields as follows:

First - First()
Last- Last()
Size - Size()

4. Drop `Measure Names` in the Filters (choose First along Category , Last along Category , Index along Category, Size along Category)
5. Drop `Measure Values` in **Text**
Add a table calculation for all the fields (Set it to Specific Dimensions - Category)

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_6/4.png?raw=true)

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_6/5.png?raw=true)

-----

### ✅ **Report 5: Lookup and Previous Value Report**

1. Ceate Calculated fields:
Lookup - `LOOKUP(ATTR([Category]), -1)`
Previous Value - `Previous_Value("") + 
"," + 
ATTR([Category])`

2. Drag and drop the following in rows
- Department
- Category
- Lookup 
- Previous Value

3. Add table calculations to the fields Lookup and Previous Value as below

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_6/6.png?raw=true)

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_6/6.2.png?raw=true)
--------

### ✅ **Report 6: Running Functions Report**

Just duplicate Report 5. 


1. Drag and drop the following in rows
- Department
- Category

2. Drop `Measure Names` in Columns

3. Create a calculated field under **Tables**. Name the field as **Running Min of Sales** and enter the below formula.

**Formula**

`RUNNING_MIN(SUM([Sales]))`

4. Create a calculated field under **Tables**. Name the field as **Running Sum of Sales** and enter the below formula.

**Formula**

`RUNNING_SUM(SUM([Sales]))`

5. Drop `Measure Names` in **Filters** and choose ( Sales, Running Min of Sales, Running Sum of Sales)
6. Drop `Measure Values` in **Text**

6. Add table configuration for (Running Min of Sales, Running Sum of Sales) as follows

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_6/7.png?raw=true)

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_6/7.2.png?raw=true)

-----

### ✅ **Report 7: Window Functions**

Duplicate report 6

1. Create a calculated fields under **Tables**. 
- Window Max - `WINDOW_MAX(SUM([Sales]))`
- Window Sum - `WINDOW_SUM(SUM([Sales]))`

2. For `Measure Names` in Filters and choose ( Sales, Window Max, Window Sum)
3. Add table configuration for (Window Max, Window Sum) as follows

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_6/8.png?raw=true)

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_6/8.2.png?raw=true)

 -----
 
 ### ✅ **Report 8: Rank Functions  Report**


Duplicate report 7

1. Create calculated field `Rank` with formula
`RANK(SUM(Sales))`
2. Just remove the fields **Window Max, Window Sum** from the filters and keep `Sales` and `Rank`

Add table configuration for Rank as follows


![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_6/9.png?raw=true)

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_6/9.2.png?raw=true)

---------

### ✅ **Report 9: Year over Year Growth Report**

1. Drop `Order Date` in Columns twice, once as **Year** and **Quarter**
2. Drop `Sales` in Rows. For the second Sum(sales) add a table calculation as below
3. Set the second Sum(sales) to Bar in Marks card 

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_6/10.png?raw=true)

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_6/10.2.png?raw=true)

------------
### ✅ **Report 10 : Sales Per State Report**

1. Drop `Region`and `State` in Rows.

2. Drop `Sales` in Columns

3. Drop the following in details and use the formulas along. (Just double click on them)
State - `TOTAL(COUNTD([State]))`
Window Sum - `WINDOW_SUM(MIN(1))`
Size - `Size()`

Add table configuration for the above fields as follows

4. Drop **Region** in Filters and choose `Central` and `South`

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_6/11.png?raw=true)

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_6/11.2.png?raw=true)

---
