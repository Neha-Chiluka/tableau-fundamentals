# 📘 Lab 14: Data Structures, Aggregation Challenges, and Level of Detail (LOD) Expressions

#### Objective:

In this lab, you will:

1. Explore the impact of data structures (tall vs. wide) on visualization in Tableau.
2. Analyze various measures across different dimensions, including population trends and bank account balances.
3. Understand common pitfalls in data aggregation, specifically when calculating ratios like "Rent per Square Foot."
4. Master the use of Level of Detail (LOD) expressions to correctly perform complex calculations and overcome aggregation challenges, ensuring accurate per-apartment metrics.
5. Apply reference lines to visualize key performance indicators over time.


---

### ✅ **Report 1: Values and years Report**

1. Drag `Measure Names` to the **Columns** and **Rows** shelf.
2. Drag `Measure Names` to **Filters**.
3. Drop `Country Name` in **Color**. Choose any country

Set the marks card to Line

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_14/1.png?raw=true)


---------

### ✅ **Report 2:Using Tall Data **

**Use Tall(country) data.**

1. Drag `Year` to the **Columns** 
2. Drag `Population` to **Rows** shelf.
3. Drop `Country Name` in **Color**. Choose any country

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_14/2.png?raw=true)

---

### ✅ **Report 3: Country by population **

1. Drag `Year` to the **Columns** 
2. Drag `Population` to **Rows** shelf.

Add formatting as per your need

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_14/3.png?raw=true)

---

### ✅ **Report 4: Namy by Bank account balance **


1. Drag `Bank Account balance` to the **Columns** shelf.
2. Drag `Name` to the **Rows** shelf.
3. Drop `Table Name` in color.

Sort it by descending order

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_14/4.png?raw=true)

----

### ✅ **Report 5: Patients in Hospital **

1. Drag `Date` to the **Columns** shelf. Set it to Day
2. Drag `Patients in Hospital` to the **Rows** shelf.
3.Set the marks card to Area.

4. Add a reference line for entire table as below.

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_14/5.png?raw=true)

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_14/5.1.png?raw=true)

-----

### ✅ **Report 6: Measures Per Apartment **

1. Drag `Measure Names` to the **Columns** shelf. Sort it by descending order
2. Drag `Apartment` to the **Rows** shelf. 

3. Drop `Measure values` to **Text**.
4. Drop `Measure Names` to **filters**

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_14/6.png?raw=true)

--------

### Report 7 : Rent per Square Foot

Duplicate the above report

1. Create the below calcualted fields

- Rent per Square Foot (wrong - AVG) - `SUM([Rent Collected]) / AVG([Square Feet])`
- Rent per Square Foot (wrong - MIN) - `SUM([Rent Collected]) / MIN([Square Feet])`
- Rent per Square Foot (wrong - SUM) - `SUM([Rent Collected]) / SUM([Square Feet])`
- Rent per Square Foot (wrong- MAX) - `SUM([Rent Collected]) / MAX([Square Feet])`

2. Sort the Measure Names to descending order

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_14/7.png?raw=true)

-----------------
### Report 8: Solving Rent per Square Foot with LOD


1. Drag `Measure Names` to the Columns shelf.Sort it by descending order
2. Drag `Apartment` to the Rows shelf. 
3. Drop `Measure values` to Text.
4. Drop `Measure Names` to filters.

- Choose Rent collected
- Square feet per apartment
- Rent Collected per Square Foot set to agrregate([Rent Collected per Square Foot])

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_14/8.png?raw=true)

--------


