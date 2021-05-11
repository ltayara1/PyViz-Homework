# Pythonic Monopoly

## Background

In this project, I built a prototype dashboard to display investment opportunities for the San Francisco market. The goal of this dashboard is to provide charts, maps, and interactive visualizations that help customers explore the data and determine if they want to invest in rental properties in San Francisco.

### Rental Analysis

The first step to building the dashboard is to work out all of the calculations and visualizations in an analysis notebook. Once the code is worked out here, it can be copied over to a dashboard code and used with Panel to create the final layout. 

#### Housing Units Per Year

In this section, I calculated the number of housing units per year and visualized the results as a bar chart using the Pandas plot function.


#### Average Gross Rent in San Francisco Per Year

In this section, I visualized the average gross rent per year to better understand the trends for rental income over time. I calculated the average (mean) gross rent per year and visualizde it as a line chart.

#### Average Sales Price Per Year

In this section, I determined the average sales price per year to better understand the sales price of the rental property over time. For example, a customer will want to know if they should expect an increase or decrease in the property value over time so they can determine how long to hold the rental property. I calculated the average (mean) `sales_price_sqr_foot` and visualized it as a bar chart.

#### Average Prices By Neighborhood

In this section, I compared the average prices by neighborhood.I grouped the data by year and by neighborhood and calculated the average (mean) `sales_price_sqr_foot`. I then, visualized the mean `sales_price_sqr_foot` per year with the neighborhood as a dropdown selector. I used hvplot to obtain the interactive dropdown selector for the neighborhood.

#### Top 10 Most Expensive Neighborhoods

In this section, I figured out which neighborhoods are the most expensive. I calculated the mean sale price for each neighborhood and then sorted the values to obtain the top 10 most expensive neighborhoods on average. I plotted the results as a bar chart.

#### Parallel Coordinates and Parallel Categories Analysis

In this section, I used plotly express to create parallel coordinates and parallel categories visualizations so that investors can interactively filter and explore various factors related to the sales price of the neighborhoods.

Using the DataFrame of Average values per neighborhood (calculated above), I created a Parallel Coordinates Plot and a Parallel Categories Plot.

#### Neighborhood Map

In this final section, I read in neighborhood location data and built an interactive map with the average prices per neighborhood. I used a scatter mapbox object from plotly express to create the visualization. I used my mapbox API key for this.

### Dashboard

After working out all of the code and analysis, I used the Panel library to build an interactive dashboard for all of the visualizations. 

Create a new `dashboard.ipynb` for your dashboard code. Copy over the code for each visualization and place this into separate functions (1 function per visualization). This will make it easier to build and modify the layout later. Each function should return the plot figure in a format that Panel can use to plot the visualization.

Sample Dashboard:

  ![dashboard-demo.gif](Images/dashboard-demo.gif)