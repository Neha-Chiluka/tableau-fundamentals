
---

### ✅ **Report 1: Basic Map Report**

1. Drag `Longitude` to the **Columns** shelf.
2. Drag `Latitude` to the **Rows** shelf.
3. Drop `City` **Detail**.


![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_12/1.png?raw=true)


### ✅ **Report 2:Dark Map**

Duplicate the above report and change the background to black use the formatting.

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_12/2.png?raw=true)

---

### ✅ **Report 3: Houses for Sale Report**

**from Real Estate**

1. Drag Longitude to the Columns shelf.
2. Drag Latitude to the Rows shelf.

Set them to Average

3. Drop Price in Size and ID in detail.

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_12/3.png?raw=true)



---

### ✅ **Report 4: Hospital and Patients Chart**


1. Drag Longitude to the Columns shelf.
2. Drag Latitude to the Rows shelf.

Set them to Average

3. Drop `Location Type` in **Color** , **Size** and **shape**
4. Drop `ID` in **Detail**

Click on the shape card and change the shapes for Hospital and Patient Residence as per your choice

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_12/4.png?raw=true)



----

### ✅ **Report 5: Lines **

1. Drag `Longitude` to the **Columns** shelf.
2. Drag `Latitude` to the **Rows** shelf.
3.Drop `Line` and `Id` in **Detail**.

For Line , set the measure to collect.

4. Create a calculated field 

**Distance to the Hospital**

`
DISTANCE(
    MAKEPOINT([Hospital Latitude], [Hospital Longitude]),
    MAKEPOINT([Latitude], [Longitude]),
    'mi'
)
`


Drop this field in Tooltip

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_12/5.png?raw=true)



-----

### ✅ **Report 6: Buffer **

1. Drag `Longitude` to the **Columns** shelf.
2. Drag `Latitude` to the **Rows** shelf. Twice

Click on the arrow of Latitude and set to dual axis

3. In one of the latitude. drop ID latitude , longitude and location type in detail. Set the marks card to circle
4. In other latitude drop Hospital radius to Detail. Set the measure to collect.

For that create a calculated field using the below formula

**Formula**

`IF [Location Type] == "Hospital"
THEN BUFFER(MAKEPOINT([Latitude], [Longitude]), 3, 'mi')
END`

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_12/6.png?raw=true)

--------

### Report 7 : Average House Prices

1. Drag `Longitude` to the **Columns** shelf.
2. Drag `Latitude` to the **Rows** shelf. 
3. Create a group for Zip and configure as below

78702, 78717, 78721 and 16 more
78732, 78734, 78735 and 4 more
Other

4. Drop `Zip code` group field in Color
5. Drop `Price` in label

![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_12/7.png?raw=true)

-----------------
### Report 8:  Average House Prices by Region


1. Drag `Longitude` to the **Columns** shelf.
2. Drag` Latitude` to the **Rows** shelf. 
3. Drop `Region` in **Color**
4. Drop `Price` in **Label** and change its measure to average


![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_12/8.png?raw=true)

--------

### Report 9:  Dual Axis Map


1. Drag `Longitude` to the **Columns** shelf.
2. Drag `Latitude` to the **Rows** shelf.  (Twice)
3. In one of the latitude. Drop it in Color and State in Detail
4. In other latitude drop Sales in Size and Postal code in detail. Set Marks card to circle.


![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_12/9.png?raw=true)

----------
### Report 10: Washed Out Map

1. Drag **Longitude** to the **Columns** shelf.
2. Drag **Latitude** to the **Rows** shelf. 
3. Drop `Profit` in **Color** and State in **Detail**


![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_12/10.png?raw=true)

-------------
### Report 11: Number of Patients per Room.
1. Drag `X` to the **Columns** shelf.
2. Drag `Floor` and `Y` to the **Rows** shelf. 
3. Drop `Number of Patients` in Size. Change the marks card to circle.


![](https://github.com/Neha-Chiluka/tableau-fundamentals/blob/master/pic_12/11.png?raw=true)

----------

