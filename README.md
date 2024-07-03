# Zomato Global Restaurant Data Analysis - Power BI Report
============================================================

This repository contains the Power BI report visualizing Zomato restaurant data across 6 continents. The dashboard provides insights into various aspects of restaurant performance, including customer ratings, average cost of two  people, cuisine served, and online delivery availability etc.

## Data Sources
-------------

* **Restaurant Data:** A appended datasets of 6 regions including Asia, Africa, Europe, Oceania, SAM and NAM.
* **Cuisine Data:** A table listing different cuisines served by restaurants.
* **Country Code Data:** A table mapping country codes to continent names.

## Data Preparation and Processing
-----------------

### Power Query
* Appended Continent Data: Datasets of 6 regions including Asia, Africa, Europe, Oceania, SAM and NAM was appended to create a new table zomato global.
* Then other three table fact table, cusines and country code was loaded in power query.

#### 1. Zomato Global

* Misspelled words are correced(eg: Brasí_lia to Brasília) using replace value.
* Removed unnecessary columns.
* Created 'Restaurant Name' and 'Address' from a single column using split columns.
* Removed blank and duplicate records.
* Changed data types to appropriate ones.

#### 2. Cusines

* Misspelled words are correced(eg: "Sí£o Paulo" to "São Paulo") using replace value.
* Removed all unnecessary columns that are duplicated from zomato global table.
* Converted Cusines seved from column level to row level using split column into rows.
* Changed data types to appropriate ones.
* Replaced comma to nothing in cusine column.

#### 3. Country Code

* Removed blank and duplicate rows.
* Merged Queries to add continent in country code table from zomato global tablw.
* Converted Cusines seved from column level to row level using split column into rows.

#### 4. Fact Table

* It has infromation about restaurent rating, price, Has table booking etc.
* created a custom column that shows raitng color like dark green, green, yellow, orange based on rating. 
* Created a conditional column (to_rupee) that convert other currency to INR to maintain data consistency.
* Created another custom column that shows avergae cost of two people in INR. I got it by multiplying cost to to_rupee column

### DAX
* #### Measures: Total Cities, Total Restaurent, Total Cusines Served.



## Power BI Report
-------------------

The Power BI dashboard consists of two pages and there is a button created using boomark to navigate between the pages.

### Page 1: 

* **Distribution of Restaurents Across Continents:** Bar/Map chart showing this, sorted in ascending order.There is button created using bookmark to change the visual from bar to map.
* **Restaurents Offering Online Delivery:** Pie chart showing the no. of restaurents offer online delivery or not.
* **Restaurents Offering Table Booking:** Donut chart showing the no. of restaurents offer table booking or not.
* **Average Rating and Total Restaurant by Rating Color:** Area chart showing the average rating and total number of restaurants for each rating color category (dark green, green, yellow, orange, red).
* **Total Restaurants:** Card displaying the total number of restaurants in the dataset.
* **Total Cities:** Card displaying the total number of cities with restaurants.
* **Cuisines Served:** Card displaying the total number of cuisines served.
* **Bookmarks:** Allows users to switch between bar chart and map visualizations.
* **Slicers:** Allow users to filter data based on location, rating color, and online delivery availability.

### Page 2: 

* **Total Cuisines Served by Restaurants:** A bar chart that shows the number of cusines served by different restaurants. The restaurants are ranked in descending order of the number of cusines they serve.
* **Avg. Cost Of Two By Restaurant Name:** A bar chart that shows the average cost of two people dining at different restaurants.
* **Restaurants With Highest Average Customer Ratings:** A tree map is showing this.The top rated restaurants have a rating of 4.90.
* **Popular Cusines:** Bar chart is showing popular cusines, cusines that are served by most restaurents, the result is in descending order.
* **Total Restaurants:** Card displaying the total number of restaurants in the dataset.
* **Total Cities:** Card displaying the total number of cities with restaurants.
* **Cuisines Served:** Card displaying the total number of cuisines served.
* **Slicers:** Allow users to filter data based on location, Online delivery availability and restaurent.

## Visualizations
--------------

The dashboard utilizes various charts and visualizations:

* Bar Chart
* Map
* Pie Chart
* Area Chart
* Treemap

## Measures
---------

* **Total Restaurants:** Calculated by counting the number of unique restaurant IDs.
* **Total Cities:** Calculated by counting the number of unique cities.
* **Cuisines Served:** Calculated by counting the number of distinct cuisines.

## Instructions
------------

1. Clone or download this repository.
2. Open the Power BI desktop file (.pbix).
3. The dashboard will automatically load with the visualizations and data.
4. Explore the dashboard by interacting with slicers, bookmarks, and other interactive elements.

This report provides valuable insights into Zomato restaurant data, allowing users to analyze restaurant performance, identify popular cuisines, Cusines Served by restaurents and track online delivery trends etc.  
