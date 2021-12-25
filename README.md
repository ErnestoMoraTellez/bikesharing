# Bike_sharing_Analysis


## Overview of Bike_sharing_Analysis

We want to perform an analysis for a future bike sharing bussiness similar to the one in NYC. We have some investors and we will look at the data of NYC bussiness to determine how our company should work in our town. 

[link to dashboard] (https://public.tableau.com/app/profile/ernesto.mora.tellez)

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
    
With the new dataset we used Tableau to create some visualizations and analisys.

The first viz that we create shows the time that the user use the bike in average. We can see that most of the people use the bikes for 5 minutes. And it's not common to use the bikes for more than an hour. So they use to do short trips.

![image](https://user-images.githubusercontent.com/88845919/147390428-298ad254-2d7b-44ff-9881-246fd09c6e5f.png)

As second Viz, we create the same graph but differenciating by Gender. With this analysis, we can see that most of the users are Male.

![Checkout Times by Gender](https://user-images.githubusercontent.com/88845919/147390568-aa1d55f1-5df5-4b43-b973-87de629ba429.PNG)

Then we looked at the number of trips per hour and day. This tell us that the high demand of users are from monday to friday in different hours, 7AM to 9AM and 5PM to 7PM. With this we can have and spected amount of bikes that we need to consider.

![Trips by Weekday for Each Hour](https://user-images.githubusercontent.com/88845919/147390637-2ad67932-f83f-4e57-bf19-05103475d1a3.PNG)

Now looking at the same info but by gender, most of the users are Male.

![Trips by Gender (Weekday per Hour)](https://user-images.githubusercontent.com/88845919/147390641-3c8e80b7-4367-4311-add8-2979765213a6.PNG)

Then we can see the usage by gender and usertype on different days of the week. Most of the users are Male as we alredy know, and the higher demand day is on thursday. The new information that we get is that the subscribers are the ones that use more the bikes.

![User Trips by Gender by Weekday](https://user-images.githubusercontent.com/88845919/147390925-1ed4471c-1291-4535-b6f2-cd489f3a0780.PNG)

Other data that we can get, is the users by age and the relation with the trip duration. We can notice that the youngest users use more time the bike.

![image](https://user-images.githubusercontent.com/88845919/147391654-c26ad4fb-7bc3-4ef3-9f5c-191c70d7e08c.png)

And here we can see the places where the users start the trips and the total number of rides, wich age they have and the share by gender.

![image](https://user-images.githubusercontent.com/88845919/147391669-8d5bef7a-ba71-42a1-8079-4370ac27ca04.png)

### Resume

As summary, we can say that we can use the date from NYC to estimate at first the number of user we can get. Also que time a trip takes to estimate the number on bikes we need to identiy the demand.

We can look for the places that are represented by the starting locations and compare this atractions or places localy to find good places to put the bikes.

We can spect same share per gender and age, so we can plan some maintence time also using the time with less trafic or usage of the bikes.

With this information we can get some amount of revenue. We can look for this information an create a map with the better locations. Probably we can save costs with this analysis.

Also, we can link the usage and the map, to create some rotation of the bikes and maximize the lifetime and the maintenance.
