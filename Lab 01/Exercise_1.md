Alright! Let's begin by designing **Lab 1: Creating Your First Interactive Report in Tableau** using the provided Superstore data.

---

## 📘 **Lab 1: Creating Your First Interactive Report - Sales Overview**

### Objective:
In this lab, you will:
- Connect Tableau to the Superstore dataset!
- Create an interactive report showing Sales by Category and Region
- Add basic interactivity (filter, tooltip, and formatting)

---

### ✅ **Step 1: Open Tableau and Connect to Data**

1. Open **Tableau Desktop**.
2. From the home screen, click **"Microsoft Excel"** if you saved the dataset as an Excel file or **"Text File"** if it's a CSV.
3. Locate your dataset file (Superstore_Lab1.csv or Excel).
![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/Lab1/1.png?raw=true)
4. Click **Open**. 

---

### ✅ **Step 2: Load the Data into Tableau**

1. Tableau will automatically load the data into the **Data Source** tab.
2. Verify that all columns are loaded correctly (e.g., Sales, Profit, Region, etc.).
3. Click **Sheet 1** at the bottom to start creating your report.

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/Lab1/2.png?raw=true)

---

### ✅ **Report 1: Create a Sales by Department **

1. Drag `Sales` to the **Columns** shelf.
2. Drag `Department`  to the **Rows** shelf.

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_1/1.png?raw=true)

Double tap in sheet 1 and rename it as **Sales by Department**


---

### ✅ **Report 2: Sales by Region and Department**


**Steps**:
1. Go to a new worksheet and name it **Sales vs. Profit**.
2. Drag `Sales` to **Columns**.
3. Drag `Region` and `Department` to **Rows**.

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_1/2.png?raw=true)

---

### ✅ **Report 3: Sales of Department by Region ( Bar Chart - Stacked)**


**Steps**:
1. Create a new worksheet called **Sales by Department ( Bar Chart - Stacked)**.
2. Drag `Department` to **Rows**.
3. Drag `Sales` to **Columns`.
4. Drag `Region` to color in the Marks card.

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_1/3.png?raw=true)

Double tap on sheet 3 and rename it as **Sales of Department by Region ( Bar Chart - Stacked)**

### ✅ **Report 4: Sales over Time( Quarter )**


**Steps**:
1. Create a new worksheet called **Sales over Time( Quarter )**.
2. Drag `Sales` to **Rows**.
3. Drag `Order Date` to **Columns**.
4. Click on the arrow of the column(Order date) and choose quarter from the dropdown.

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_1/Screenshot%202025-06-09%20153216.png?raw=true)

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_1/6.png?raw=true)
Rename the sheet as Sales over Time( Quarter )

### ✅ **Report 5: Sales over Time by Region**


**Steps**:
1. Create a new worksheet called **Sales over Time by Region**.
2. Drag `Sales` to **Rows**.
3. Drag `Order Date` to  **Columns**
4. Click on the arrow of the column(Order date) and choose quarter from the dropdown.
5. Drag Region on the color option on the Marks Card

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_1/7.png?raw=true)

### ✅ **Report 6: Sales over Time by Category **


**Steps**:
1. Create a new worksheet called **Sales over Time by Category**
2. Drag `Sales` and `Category` to **Rows**.
3. Drag `Order Date` to **Columns**.
4. Click on the arrow of the column (Order date) and choose quarter from the dropdown.

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_1/8.png?raw=true)

### ✅ **Report 7: Sales by State **


**Steps**:
1. Create a new worksheet called **Sales by State**
2. Drag `Latitude` to **Rows**.
3. Drag `Longitude` to **Columns**.
4. Drag and drop `Sales` in **color** option on the **Marks** card
5. Drag and drop `State` in the **detail** option on the **Marks** card

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_1/9.png?raw=true)

### ✅ **Report 8: Sales by Postal Code **


**Steps**:
1. Create a new worksheet called **Sales by Postal Code**
2. Drag `Latitude` to **Rows**.
3. Drag `Longitude` to **Columns**.
4. Drag and drop `Sales` in Size option on the **Marks** card
5. Drag and drop `Postal Code` in the detail option on the **Marks** card
6. Drag and drop `Profit` in the Color option on the **Marks** Card

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_1/10.png?raw=true)

### ✅ **Report 9: Density of Orders**


**Steps**:
1. Create a new worksheet called **Density of Orders**
2. Drag `Latitude` to **Rows**.
3. Drag `Longitude` to **Columns**.
4. Drag and drop `Postal Code` in the detail option on the **Marks** card

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_1/11.png?raw=true)

### ✅ **Dashboard: Superstore Sales**


**Steps**:
1. Click on the **dashboard** option located on the **Title** bar.
2. Select **new dashboard (** you will land on a empty dashboard)
3. From the existing sheets list on the left pane, Drag and drop the following sheets
- Sales by Department
- Sales over Time(Quarter)
- Sales by Postal Code

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_1/12.png?raw=true)



---

Next , we shall continue with our lab2 using the same dataset.
