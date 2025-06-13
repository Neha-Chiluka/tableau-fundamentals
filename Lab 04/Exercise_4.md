# 📘 Lab 4: Rental Property Performance Analysis

#### Objective:

In this lab, you will:

1. Connect Tableau to rental property data.
2. Analyze rent per building and room, total rent per floor, and discount percentages at various levels.
3. Create a rental calendar to track bookings and identify "free nights."
4. Evaluate revenue per guest to identify key insights.
5. Utilize calculated fields for data preparation and advanced analysis.


---

### ✅ **Report 1: Rent per Building & Room Report**

1. Drag **Rent** to the Columns shelf.
2. Create a calculated field under **Tables**. Name the field as **Building** and enter the below formula.

**Formula**

`SPLIT([Rental Property], "-", 2)`
3. Create a calculated field under Tables. Name the field as **Room** and enter the below formula.

**Formula**

`SPLIT([Rental Property], "-", 1)`

2. Drag `Building` and `Room` to the **Rows**.

Double tap in sheet 1 and rename it as **Rent per Building & Room**


![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_4/1.png?raw=true)


---

### ✅ **Report 2: Total Rent per Floor**


**Steps**:
1. Go to a new worksheet and name it **Total Rent per Floor**.
2. Create a calculated field under Tables. Name the field as **Floor** and enter the below formula.

**Formula**

```python
IF LEFT([Room], 1) = "1"
THEN "First Floor" 
ELSEIF LEFT([Room], 1) = "2" 
THEN "Second Floor" 
END
```
Then Drag the `Floor` to **Columns**
3. Drag `Rent` to **Rows**.

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_4/2.png?raw=true)

---

### ✅ **Report 3: Discount % per Rental Report**


1. Create a calculated field under **Tables**. Name the field as **End Date** and enter the below formula.

**Formula**

`DATE([End] + ", 2020")`

2. Create a calculated field under **Tables**. Name the field as **Start Date** and enter the below formula.

**Formula**

`DATE([Start] + ", 2020")`

3. Create a calculated field under **Tables**. Name the field as **Full Name** and enter the below formula.

**Formula**

`[First] + " " + [Last]`

4. Create a calculated field under **Tables**. Name the field as **Discount %** and enter the below formula.

**Formula**

`SUM([Discount]) / SUM([Rent])`

5. Drag and drop the following to **Rows**:
- Building
- Room
- Full Name 
- Start 
- End 

6. Drop `Measure Names` to **Columns**
7. Drop `Measure Names` to **Filters** and choose `Discount`, `Discount %` & `Rent`
8. Drop `Measure values` to **Labels**

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_4/3.png?raw=true)

----

### ✅ **Report 4: Discount % per Room Report**

Just duplicate Report 3 and remove start and end dates from Rows.


![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_4/4.png?raw=true)

-----

### ✅ **Report 5: Overal Discount % Report**

Just duplicate Report 4 and remove all the fields from Rows.To understand the overall discount percentage.

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_4/5.png?raw=true)

--------
### ✅ **Report 6: Overal Discount % (Aggregate v. Row Level) Report**

Just duplicate Report 5. 

1. Change the view to `Fit Width`
2. Create a calculated field under **Discount%**. Name the field as **Discount % (row level)** and enter the below formula.

**Formula**

`[Discount] / [Rent]`
3. Now select Discount % (row level) in the Filter that is already existing(i.e Measure Names)

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_4/6.png?raw=true)

-----

### ✅ **Report 7: Rental Calendar Report**

1. Drag and drop the following to **Rows**:
- Building
- Room
2. Drop `Start Date` in **Columns**
3. Create a calculated field under **Discount % (row level)**. Name the field as **Nights Rented** and enter the below formula.

**Formula**

`DATEDIFF('day', [Start Date], [End Date])`

 Drop this field on **Size**
 
 4. Drop `Full Name` on **Label**
 5. Click on **Label** and change the alignment to **Middle Center**. And **Show mark Label** is ticked


![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_4/7.png?raw=true)

 -----
 ### ✅ **Report 8: Free Night Analysis Report**

**Just duplicate report 7**. 

1. Right click on a empty space of columns (Left pane). Create Parameter and follow the below configuration.

**Note:-**
- If it automatically picks a random date we can still edit it later.

- Once you have click on ok.

- You will see the parameter created. Now click on the arrow of **Free Night** and click on **show parameter**

- Now you can set the date as **12-12-2020**

2. Create a calculated field under **Tables**. Name the field as **Gets Free Night** and enter the below formula.

**Formula**

`[Free Night] >= [Start Date]
AND
[Free Night] <= [End Date]`

Pull this field into **Color**.

3. Right click on the bottom axis and create a reference line. Follow the below configuration.

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_4/8.png?raw=true)

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_4/8.2.png?raw=true)

---------
### ✅ **Report 9: Revenue per Guest Report**

1. Create a calculated field under **Rent**. Name the field as **Revenue** and enter the below formula.

**Formula**

`[Rent] - [Discount] + ([Tax per Night] * [Nights Rented])`

Drop this is Columns

2. Drop Full Name in Rows
3. Drop Revenue on Color.

Now Double click on Revenue and enter the below formula.
`SUM([Revenue]) < 1500`


![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_4/9.png?raw=true)


------------
