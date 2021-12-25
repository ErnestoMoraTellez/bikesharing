# Bike_sharing_Analysis


## Overview of Bike_sharing_Analysis

We want to perform an analysis for a future bike sharing bussiness similar to the one in NYC. We have some investors and we will look at the data of NYC bussiness to determine how our company should work in our town. 

### Purpose

We need to create a presentation for our invertors. We will use Tableau to show some visualizations of our data analysis.

### Bike_sharing_Analysis Results

For the first step we need to modify the data. Specially we change the data type of the tripduration from int64 to data time. Then we create a mew CSV file to perform the analysis.

    import pandas as pd

    # 1. Create a DataFrame for the 201908-citibike-tripdata data. 
    citibike_data_df = pd.read_csv("201908-citibike-tripdata.csv")
    citibike_data_df.head()
    
![image](https://user-images.githubusercontent.com/88845919/147390329-32316ccf-8103-46b3-aca6-418c23e59f98.png)

    # 2. Check the datatypes of your columns. 
    citibike_data_df.dtypes
    
![image](https://user-images.githubusercontent.com/88845919/147390340-7f217841-3a8a-468e-84db-e54de61fdce3.png)

    # 3. Convert the 'tripduration' column to datetime datatype.
    citibike_data_df['tripduration'] = pd.to_datetime(citibike_data_df['tripduration'],unit='s')
    
    # 4. Check the datatypes of your columns. 
    citibike_data_df.dtypes
    
![image](https://user-images.githubusercontent.com/88845919/147390356-de4ddd15-a7a6-4428-bc01-2f9a9cca4a3b.png)
    
    # 5. Export the Dataframe as a new CSV file without the index.
    citibike_data_df.to_csv('citibike.csv',index=False)
    
Whit the new dataset we used Tableau to create some visualizations and analisys.

The first viz that we create shows the 
