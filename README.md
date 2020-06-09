For this workshop we will be using population data, median household income data and map data. The tool we will be using to collect all data is SimplyAnalytics.

1.	Log into SimplyAnalytics as a guest from the library website: http://libguides.gatech.edu/az.php?a=s
2.	The page will prompt you with a New Project box. Search the location Georgia here.
3.	Then choose #Population and Median Household Income
4.	Create Project
 
5.	Name project: (on the top left) double click Current Project: New Project -> rename it in the pop-up box
6.	Add extra years of Population and Median Household Income to the table: 
a.	Comparison Table -> Population Data -> 2018-2017/2016 -> Choose Population
b.	Income -> 2018/2017/2016 ->Choose Median Household Income
 
c.	After added, the final view should look like this:
 

7.	On the right-side of the window -> New View  
8.	Ranking Table -> Create
 
9.	Click on the new Ranking tab generated
 
10.	Change the variables on top: top 100 / Counties
 
11.	Export
 
12.	Fetch map data
 
13.	With the variables, SimplyAnalytics will generate the map below.
 
14.	Export shapefile. It will be emailed to you after you fill out the form.
 


Tableau Visualization
1.	Import Data
a.	Import Excel data
 
b.	Import Shapefile
 

2.	Join two tables by name (county names)
 

3.	After the data is joint, switch to a sheet to create your visualization! 
4.	Drag and drop Geometry on the sheet
 
5.	Drag and drop name to the map so that now if you hover over on the map you will be able to see individual counties highlighted.
 
6.	Drag and drop Median Household Income 2019 on color tab under marks so that the map is colored by the value of the 2019 median income.
 
7.	Customize the map color: click on Color, and then on the pop-up box click on Edit Colors, click on the drop-down button behind Palette (Automatic) -> choose the color palette you like from the drop-down options.Click OK when done.
 
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
 
