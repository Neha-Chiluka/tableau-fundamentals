
# 📘 Lab 5: Financial Risk & Loan Portfolio Analysis

#### Objective:

In this lab, you will:

1. Connect Tableau to financial data.
2. Analyze orders by state using various reference lines.
3. Identify and assess member credit risk and loan history.
4. Explore average loan distribution and credit scores across different portfolios and loan types.
5. Master the application of Level of Detail (LOD) expressions (FIXED, INCLUDE, EXCLUDE) for advanced calculations.

---

### ✅ **Report 1: Orders by State with Average Reference Line Report**

1. Drag **Orders** to the Columns shelf.
2. Drop **State** in Rows 

3. Create a refernce line for Orders axis. Use the configuration as below


Double tap in sheet 1 and rename it as **Orders by State with Average Reference Line**

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_5/1.png?raw=true)

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_5/1.2.png?raw=true)

---

### ✅ **Report 2: Orders by State with Calculated Reference Line**


**Steps**:

Duplicate the report 1. 
1. Just change the configuration for the reference line as below

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_5/2.png?raw=true)

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_5/2.2.png?raw=true)

---

### ✅ **Report 3:  Member Ever at Risk? Report**


1. Create a calculated field under **Tables**. Name the field as **Member Ever at Risk?** and enter the below formula.

**Formula**

`{FIXED [Member ID] : MIN([Credit Score])} < 550`

2. Drag and drop the following in rows
- Member ID
- Member Name
- Loan Type
- Date ( Make sure to keep it exact date and discrete)
- Member Ever at Risk

3. Drop `Measure Names` in Column and then drop it in the **filters** and choose `Balance` and `Credit Score` from the list.
4, Drop `Member ID` in the **Filters** ( From the list choose the numbers (158,479,576))
5. Drop `Measure Values` in **Label**


![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_5/3.png?raw=true)

----

### ✅ **Report 4:  How Many Members Ever at Risk by Portfolio Report**

1. Drop `Member ID` to **Columns** ( Choose the aggregate as ** CountDistinct** from the list)
2. Drop `Portfolio` in **Rows**
3. Drop `Member Ever at Risk?` to Color card

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_5/4.png?raw=true)

-----

### ✅ **Report 5: Member & Loan History Report**

1. Drag and drop the following in **rows**
- Member ID
- Member Name
- Loan Number
- Loan Type
- Date ( Make sure to keep it exact date and discrete)

2. Drop `Member ID` in Filters and choose the numbers(14827, 16024, 16070)
3. Drop `Balance` in Label card

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_5/5.png?raw=true)

--------
### ✅ **Report 6: Most Recent Balance Report**

Just duplicate Report 5. 


1. Create a calculated field under **Tables**. Name the field as **Latest Date per Member/Loan** and enter the below formula.

**Formula**

`{FIXED [Member ID],[Loan Number] : MAX([Date])} = [Date]`

Drop this field in rows along other fields.

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_5/6.png?raw=true)

-----

### ✅ **Report 7:  Average Loans per Member Report**

1. Drag and drop the `Latitude` to **Rows**:
2. Drop `Longititude` in **Columns**
3. Create a calculated field under **Measures**. Name the field as **Number of Loans per Member** and enter the below formula.

**Formula**

`{INCLUDE [Member ID] : COUNTD([Loan Number])}`

Drop this field on **Color**

4. Drop `State` on **Detail**

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_5/7.png?raw=true)

 -----
 ### ✅ **Report 8: State by Loans  Report**


1. Drop `State` and `Member ID` in Rows
2. Drop `State` in **Filters** and choose `North Dakota`
3. Drop `Loan Number` in Text and change the aggregate to **CountDistinct**


![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_5/8.png?raw=true)

---------
### ✅ **Report 9: Average Credit Scores by Loan Type Report**

1. Drop `Portfolio` and `Loan Type` in Rows.
2. Drop `Credit Score` in **Text** card set it to Average as aggregate.


![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_5/9.png?raw=true)

------------
### ✅ **Report 10 : Avg Credit Scores Report**

1. Drop `Portfolio` and `Loan Type` in Rows.

2. Create calculated field '**Average Credit Score Excluding Loan Type**' use the below formula

`{EXCLUDE [Loan Type] : AVG([Credit Score])}`

2. Drop `Measure Names` in columns and in filters choose `Average Credit Score Excluding Loan Type` and 'Credit Score'
2. Drop `Measure Values` in **Text** 

For `Credit Score` change the aggregate to **Average**


![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_5/10.png?raw=true)

---
### ✅ **Report 11 : Difference from Overall Portfolio Average Report**

1. Create a calculated field under **Measures**. Name the field as **Difference from Portfolio Average** and enter the below formula.

**Formula**

`AVG([Credit Score]) - AVG([Average Credit Score Excluding Loan Type])`

Drop this in Columns
2. Drop `Portfolio` and `Loan Type` in Rows.
3. Drop `Difference from Portfolio Average` to **Label**
4. Drop `Measure Names` in columns and in filters choose `Average Credit Score Excluding Loan Type` and `Credit Score`

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_5/11.png?raw=true)

--------

