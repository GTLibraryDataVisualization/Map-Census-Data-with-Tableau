## For this workshop we will be using population data, median household income data and map data. The tool we will be using to collect all data is SimplyAnalytics.

## 1. Fetch Data from SimplyAnalytics
1).	Log into SimplyAnalytics as a guest from the library website: http://libguides.gatech.edu/az.php?a=

2).	The page will prompt you with a New Project box. Search the location Georgia here.

3).	Then choose #Population and Median Household Income

4).	Create Project

   ![image](https://user-images.githubusercontent.com/37058499/84200477-e26ddb00-aa74-11ea-92ea-c0abde7b7a6d.png)

5).	Name project: (on the top left) double click Current Project: New Project -> rename it in the pop-up box

6).	Add extra years of Population and Median Household Income to the table: 

   a.	Comparison Table -> Population Data -> 2018/2017/2016 -> Choose Population

   b.	Income -> 2018/2017/2016 ->Choose Median Household Income

   ![image](https://user-images.githubusercontent.com/37058499/84200433-cf5b0b00-aa74-11ea-964c-d06ec909f17c.png)
 
   c.	After added, the final view should look like this:

   ![image](https://user-images.githubusercontent.com/37058499/84200655-2cef5780-aa75-11ea-9870-9ab8cd1fc864.png)

7.	On the right-side of the window -> New View  

   ![image](https://user-images.githubusercontent.com/37058499/84201061-b2730780-aa75-11ea-9e1d-e25546324e63.png)

8.	Ranking Table -> Create

   ![image](https://user-images.githubusercontent.com/37058499/84201099-c454aa80-aa75-11ea-8714-412b2a31e4e9.png)

9.	Click on the new Ranking tab generated

   ![image](https://user-images.githubusercontent.com/37058499/84201152-ddf5f200-aa75-11ea-92da-dae961d896b3.png)
 
10.	Change the variables on top: top 100 / Counties

   ![image](https://user-images.githubusercontent.com/37058499/84201301-ec440e00-aa75-11ea-9659-42dc1d375250.png)
 
11.	Export

   ![image](https://user-images.githubusercontent.com/37058499/84201512-fd8d1a80-aa75-11ea-8508-58e485ff204c.png)
 
12.	Fetch map data. Go back to Map, and then select the variable you want to map, if applicable.

   ![image](https://user-images.githubusercontent.com/37058499/84202192-34fbc700-aa76-11ea-862d-758fb04e8b36.png)

13.	With the variables, SimplyAnalytics will generate the map below.
 
   ![image](https://user-images.githubusercontent.com/37058499/84202458-49d85a80-aa76-11ea-85d8-d8eefff97d82.png)

14.	Export shapefile. It will be emailed to you after you fill out the form.
 
   ![image](https://user-images.githubusercontent.com/37058499/84202737-5f4d8480-aa76-11ea-93ca-634451400dfa.png)


# Tableau Visualization
1.	Import Data
a.	Import Excel data
 
 ![image](https://user-images.githubusercontent.com/37058499/84203503-8bb5d080-aa77-11ea-9882-5ef0a45b1350.png)

b.	Import Shapefile
 
 ![image](https://user-images.githubusercontent.com/37058499/84203539-9d977380-aa77-11ea-970b-b191cb330b1f.png)

2.	Join two tables by name (county names)
 
 ![image](https://user-images.githubusercontent.com/37058499/84203573-abe58f80-aa77-11ea-9b09-3a1377712816.png)

3.	After the data is joint, switch to a sheet to create your visualization! 

4.	Drag and drop Geometry on the sheet
 
 ![image](https://user-images.githubusercontent.com/37058499/84203633-c0c22300-aa77-11ea-8ccf-6bb05393283d.png)

5.	Drag and drop name to the map so that now if you hover over on the map you will be able to see individual counties highlighted.
 
 ![image](https://user-images.githubusercontent.com/37058499/84203666-d1729900-aa77-11ea-95d4-a8c10dc9b292.png)

6.	Drag and drop Median Household Income 2019 on color tab under marks so that the map is colored by the value of the 2019 median income.
 
 ![image](https://user-images.githubusercontent.com/37058499/84203715-e9e2b380-aa77-11ea-9806-2c66394987d3.png)

7.	Customize the map color: click on Color, and then on the pop-up box click on Edit Colors, click on the drop-down button behind Palette (Automatic) -> choose the color palette you like from the drop-down options.Click OK when done.
 
 ![image](https://user-images.githubusercontent.com/37058499/84203738-f9fa9300-aa77-11ea-9f25-b715b1957956.png)

8.	Now you have finished creating the first frame of the map. Go down to the bottom of the page and click on the the tab on the right side of “sheet 1” to create a second sheet.
  
9.	Drag and drop name to the Columns.
 
10.	Drag and drop Measure Values into Rows. Then all variables will appear under the marks. Drag and drop the unwanted once out of the space. Now you should have Population 2016-2019 data under measure values only.
 
11.	Drag and drop Measure names into Columns so that all stacked bars are shifted side by side.
 
12.	Drag and drop Measure Values on Color so that all bars are colored by its values.
 
13.	To have all values showing on top of the bars, drag and drop Measure Values on Label under Marks.
 
14.	Now we have completed the second sheet. Go back to the first sheet and use Tooltip to insert it. 
Tooltip -> Insert on the tip right of the edit box -> Sheet 2 -> OK
 
15.	 To change the background map to a dark mode, go to Map -> Map Layers.  

16.	On the left sidebar, change the background style to Dark.
 
17.	Your final map should look like below:
 
