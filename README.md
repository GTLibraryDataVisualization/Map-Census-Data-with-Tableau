# Map Census Data with Tableau

The United States Census is one of the most widely used data sources in all of data science and data visualization. This training will run through the process of gathering, modifying, and visualizing census data. 
End Product should look like this:
 
   ![image](https://user-images.githubusercontent.com/37058499/64698457-ebdbff80-d470-11e9-9570-babaa0cfd6e1.png)

## STEP ONE: Gathering Data

In this training we will be using American FactFinder (https://factfinder.census.gov/faces/nav/jsf/pages/index.xhtml). American FactFinder is the best source of all Census data. The website allows you to query data to meet almost all of your needs.
How to Query
### 1.	When you are on their website, click on Advanced Search
 
 ![image](https://user-images.githubusercontent.com/37058499/64698820-93f1c880-d471-11e9-9be7-8c5fa9a07bc1.png)

Note: This is the main page for Querying data. The four boxes on the left-hand side will allow us to filter the data to suit our needs. For this training we will be using data that consists of the median household income in Georgia by county and the median age in Georgia by county. To do this, click on topics and select People ->Basic Count/Estimate -> Resident Population. 

### 2.	Filter this data down to Georgia Counties. To do this:
   a.	click on Add/Remove Geographies, 
   b.	Select Counties, 
   c.	Select Georgia, and then select all counties. 
 You should end up with the following: 
 
 ![image](https://user-images.githubusercontent.com/37058499/64698900-bbe12c00-d471-11e9-8ad6-7407fc5af6ed.png)

### 3.	Select the right dataset on the result list. 
Click on the second dataset. It is titled Annual Estimates of Resident Population: April 1,2010 to July 1,2017. You should see something like the following:
 
![image](https://user-images.githubusercontent.com/37058499/64698992-e8954380-d471-11e9-99e9-77497ad473ae.png)

### 4.	Gather the map data. To do this:
   a.	click on create a map. (American FactFinder will ask you to click on a data. For this case it does not really matter, but I will select Population Estimate 2017.) You will see the following: 

![image](https://user-images.githubusercontent.com/37058499/64699039-fb0f7d00-d471-11e9-8fa1-51c5d8dac1c5.png)

We are looking at a map that is very similar to our final product. So, why do we need to put this into tableau?? 

The reason of that, and the goal of this workshop is:
   •	create an interactive visualization with Tableau (the current view is static);
   •	customize the color, label and other details as you wish;
   •	have the option of saving it on your local machine, embed to your presentation, publication or website.
 

### 5.	View the geographical data (here called spatial data). 
   a.	We do this by clicking “download”. This creates a zip file. Open this Zip and copy all of the files into a folder on your desktop. We will be using this folder later. It will hold all our data. 
   b.	Go back to the table view. The table currently shows years 2010-2017. For readability, remove the second and third columns. To do this, click on modify table and uncheck the first two rows. 
   
### 6.	Download the data
   a.	Now hit download to get the data. Click on use the data. The data is now in a zip file. Open the zip file and copy the file called “Pep_2017_Pepannres_with_ann. Put it in the same folder as our spatial files. Open the file. You should see the following:
 
 ![image](https://user-images.githubusercontent.com/37058499/64699078-0d89b680-d472-11e9-8197-2476de35e48d.png)

### 7.	Clean the data 
The first column is something called GeoId. This will link to our spatial data from earlier. In order to make this more Readable. Delete the 1st row and 2nd columns. The 1st row are repetitive headers and the 2nd column is spatial data we do not need for this exercise. Save and rename the file as Pop_GA.  

![image](https://user-images.githubusercontent.com/37058499/64699157-2a25ee80-d472-11e9-9e60-6edfb7e287fb.png)

This data is useful, but we do not need all of it. We only need median income. Once again, use the modify table tool. Once again, go into the file and delete the first and second row. Name it Income_Ga

Now we should end up with two excel files (Pop_Ga and Income_Ga) as well as all the spatial files. 


## STEP TWO: Create Interactive Visualization in Tableau

### 1.	Open a new workbook in Tableau

### 2.	Import data 
   a.	Go to data Source add the spatial file. 
   b.	Add the 05000.shp file (drag and drop it on the top white space). 
   
### 3.	Union data sheets (essentially a JOIN statement)
   a.	Add Pop_Ga.csv file (again, drag and drop it on the top white space)
   
   ![image](https://user-images.githubusercontent.com/37058499/64699210-49bd1700-d472-11e9-8b42-4bfbfb5f0aee.png)

   b.	Select Geo Id = Id
   c.	Add the income data. Once again select add CSV and add Income_Ga.csv. You should end up with the following.
   
 ![image](https://user-images.githubusercontent.com/37058499/64699261-69543f80-d472-11e9-8cd8-8210dafb9aeb.png)

### 4.	Visualization – Create a Map
   a.	under measures and 05000.shp, double click on Geometry. 
   b.	The state of Georgia will pop up. 
   c.	Drag Geography from Pop_Ga onto the marks.

![image](https://user-images.githubusercontent.com/37058499/64699287-76712e80-d472-11e9-878f-58e8efd515c1.png)
 
### 5.	Visualization - Overlay household Income on the map
   a.	Drag Mean income from the Georgia_income.csv file and put it on color. 
   b.	Change the colors by hitting color and edit color. 
   c.	Select Red green diverging. 
   d.	Change the Opacity to 100%. 
   
![image](https://user-images.githubusercontent.com/37058499/64699328-8ab52b80-d472-11e9-9b35-ce21c0ddca62.png)

### 6.	Visualization - create a tooltip to show the household population
   a.	Create a new sheet, add name to columns and the years 2010-2017 on rows. 
   b.	Select the side by side bars graph on the show me button. 
   
   ![image](https://user-images.githubusercontent.com/37058499/64699362-9b65a180-d472-11e9-95db-0fb810cba20c.png)

   c.	go back to the map, click tooltip and insert sheet2. Filter on<Name> and expand the size of the viz in tooltip.

### 7.	Visualization – change the map layer
   a.	Click on map and select the dark theme.

 
