# Map Census Data with Tableau

The United States Census is one of the most widely used data sources in all of data science and data visualization. This training will run through the process of gathering, modifying, and visualizing census data. 
End Product should look like this:
 
   ![image](https://user-images.githubusercontent.com/37058499/64698457-ebdbff80-d470-11e9-9570-babaa0cfd6e1.png)

## STEP ONE: Gathering Data

In this training we will be using American FactFinder (https://factfinder.census.gov/faces/nav/jsf/pages/index.xhtml). American FactFinder is the best source of all Census data. The website allows you to query data to meet almost all of your needs.  

### 1.	Retrieve Census Data 
 
 ![image](https://user-images.githubusercontent.com/37058499/64698820-93f1c880-d471-11e9-9be7-8c5fa9a07bc1.png)

   a. When you are on American FactFinder website, click on Advanced Search . 
   
   b. Under Advanced Search, click on SHOW ME ALL . 
   
Note: This is the main page for Querying data. The four boxes on the left-hand side will allow us to filter the data to suit our needs. For this training we will be using data that consists of the median household income in Georgia by county and the population in Georgia by county 2012-2017. To do this:  

   c. click on Topics filter on the left top filter . 
   
   d. select People -> Basic Count/Estimate -> Resident Population . 
   
   (At this point you have successfully applied one filter. Now let's load georgraphies information) . 
   
   e. click on Georgraphies on the left fiter list . 
   
   f. on Select a Georghic Type: County-050 . 
   
   g. on Select a State: Georgia . 
   
   h. on Select one or more geographic areas and click Add to Your Selections: All Counties in Georgia . 
 Now you should end up with the following:   
 
 <img width="1049" alt="Screen Shot 2019-09-16 at 8 26 01 AM" src="https://user-images.githubusercontent.com/37058499/64957972-15739d00-d85c-11e9-8097-aa1ada6d2ffb.png">

### 2.	Select the right dataset on the result list
Click on the second dataset. It is titled Annual Estimates of Resident Population: April 1,2010 to July 1,2018. You should see something like the following:
 
 <img width="1273" alt="Screen Shot 2019-09-16 at 8 33 13 AM" src="https://user-images.githubusercontent.com/37058499/64958282-bd896600-d85c-11e9-8b8d-ff3b683fc87d.png">

### 3. Modify the table
   a. on the top left, click on the Modify Table link. See screenshot below:  

<img width="1290" alt="Screen Shot 2019-09-16 at 8 10 57 AM" src="https://user-images.githubusercontent.com/37058499/64957121-30451200-d85a-11e9-98d3-d566e0e497db.png">

   b. now you should see the screen below:    

<img width="1383" alt="Screen Shot 2019-09-16 at 8 11 11 AM" src="https://user-images.githubusercontent.com/37058499/64957127-33d89900-d85a-11e9-8cd1-ef40eca691f4.png">

   c. on top of the page, click on Download to download the dataset . 
   
### 4.	Gather the spatial data
   a.	on the top right click on Create a Map. (American FactFinder will ask you to click on a data. For this case it does not really matter which value to click on, but I will select Population Estimate 2018) . 
   
b. on the pop-up box, click on SHOW MAP. Now you will get a map like below:  

<img width="1655" alt="Screen Shot 2019-09-16 at 8 41 02 AM" src="https://user-images.githubusercontent.com/37058499/64958803-e1997700-d85d-11e9-9b56-7f7ffe0b200e.png">

We are looking at a map that is very similar to our final product. So, why do we need to put this into tableau??   

The reason of that, and the goal of this workshop is:  

   •	create an interactive visualization with Tableau (the current view is static) . 
   
   •	customize the color, label and other details as you wish . 
   
   •	have the option of saving it on your local machine, embed to your presentation, publication or website . 
   
### 5.	View the geographical data (here called spatial data). 
   a.	We do this by clicking “download”. This creates a zip file. Open this Zip and copy all of the files into a folder on your desktop. We will be using this folder later. It will hold all our data . 
   
   b.	Go back to the table view. The table currently shows years 2010-2017. For readability, remove the second and third columns. To do this, click on Modify Table and uncheck the first two rows . 
   
### 6.	Download the data
   a.	Now hit download to get the data. Click on use the data. The data is now in a zip file. Open the zip file and copy the file called “Pep_2017_Pepannres_with_ann. Put it in the same folder as our spatial files. Open the file. You should see the following:  
 
 ![image](https://user-images.githubusercontent.com/37058499/64699078-0d89b680-d472-11e9-8197-2476de35e48d.png)

### 7.	Clean the data 
The first column is something called GeoId. This will link to our spatial data from earlier. In order to make this more Readable. Delete the 1st row and 2nd columns. The 1st row are repetitive headers and the 2nd column is spatial data we do not need for this exercise. Save and rename the file as PopClean.  

![image](https://user-images.githubusercontent.com/37058499/64699157-2a25ee80-d472-11e9-9e60-6edfb7e287fb.png)

This data is useful, but we do not need all of it. We only need median income. Once again, use the modify table tool. Once again, go into the file and delete the first and second row. Name it Income_Ga . 

Now we should end up with two excel files (PopClean and IncomeClean) as well as all the spatial files . 


## STEP TWO: Create Interactive Visualization in Tableau

### 1.	Open a new workbook in Tableau

### 2.	Import data 
   a.	Go to data Source add the spatial file . 
   
   b.	Add the 05000.shp file (drag and drop it on the top white space) . 
   
### 3.	Union data sheets (essentially a JOIN statement)
   a.	Add PopClean.csv file. To do this, go up to the Add button above the file you just added:  
   
   <img width="1181" alt="Screen Shot 2019-09-16 at 9 04 34 AM" src="https://user-images.githubusercontent.com/37058499/64960543-75b90d80-d861-11e9-8011-77009b7d932d.png">

    If we want to combine two datasets by one variable, it is called Unoin in Tableau. To do this, we need to tell two tables how we want to union them . 
   b.	Select Geo Id = Id . 

 <img width="1087" alt="Screen Shot 2019-09-16 at 10 53 37 AM" src="https://user-images.githubusercontent.com/37058499/64968809-c421d880-d870-11e9-963a-1e287ef3c5f6.png">

   c.	Add the income data. Once again select add CSV and add IncomeClean.csv. You should end up with the following.
   
 <img width="1134" alt="Screen Shot 2019-09-16 at 10 54 21 AM" src="https://user-images.githubusercontent.com/37058499/64968859-dd2a8980-d870-11e9-9d62-c4c87dd1e950.png">

### 4.	Visualization – Create a Map
   a.	under measures and 05000.shp, double click on Geometry . 
   
   b.	The state of Georgia will pop up . 
   
   <img width="1403" alt="Screen Shot 2019-09-16 at 10 59 30 AM" src="https://user-images.githubusercontent.com/37058499/64969032-2975c980-d871-11e9-9f31-4e91a997fac3.png">

   c.	Drag Geography from PopClean onto the marks . 
   
 <img width="1279" alt="Screen Shot 2019-09-16 at 11 02 23 AM" src="https://user-images.githubusercontent.com/37058499/64969317-adc84c80-d871-11e9-935e-8b8b0ebd9bb5.png">
 
### 5.	Visualization - Overlay household Income on the map
   a.	Drag Mean income from the IncomeClean.csv file and put it on color . 
   
   b.	Change the colors by hitting color and edit color . 
   
   c.	Select Red green diverging . 
   
   d.	Change the Opacity to 100% . 
   
![image](https://user-images.githubusercontent.com/37058499/64699328-8ab52b80-d472-11e9-9b35-ce21c0ddca62.png)

### 6.	Visualization - create a tooltip to show the household population
   a.	Create a new sheet, add name to columns and the years 2010-2017 on rows . 
   
   b.	Select the side by side bars graph on the show me button . 
   
   ![image](https://user-images.githubusercontent.com/37058499/64699362-9b65a180-d472-11e9-95db-0fb810cba20c.png)

   c.	go back to the map, click tooltip and insert sheet2. Filter on<Name> and expand the size of the viz in tooltip . 
 
### 7.	Visualization – change the map layer
   a.	Click on Map on the top right of the menu and select the dark theme.

 
