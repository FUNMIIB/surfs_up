# surfs_up
**Overview of analysis**
The purpose of this analysis is to help W. Avy who wants to determine whether opening a surf and ice cream business in Oahu, Hawaii would be successful. The analysis is to get the temperature data from Oahu weather data stored in a SQLite database  to see the temperature trend for june and December in order determine if running the surf shop will be sustainable year round. Python, Pandas functions and methods, and SQLAlchemy were used to query the SQLite database. We filtered the date column of the Measurements table in the hawaii.sqlite database and retrieved all the temperatures for the month of June and December. The temperatures were then converted to a list and used to create a DataFrame. Finally, we generated summary statistics using the describe() method.


**Results**
The maximum and minimum temperatures for June were 85 and 64 degrees respectively while for December were 83 and 56 degrees respectively. The average temperature in June was 74.9 degrees and in December was 71 degrees. There was a total count of 1700 in June and 1517 in December. The summary statistics for June and December are shown below. (Click on the link)

![june_temp_summary](https://github.com/FUNMIIB/surfs_up/blob/main/june_temp_summary.png)
![December_temp_summary](https://github.com/FUNMIIB/surfs_up/blob/main/December_temp_summary.png)


**Summary**
Our analysis showed that the temperatures in June range from 64 to 85 degrees and in December from 56 to 83 degrees. This would be encouraging for W. Avy as these temperatures would be good for the surf and ice cream shop business to run year round. 
We could also get the precipitation in June and December to gather more weather data as shown below.

# Perform a query to retrieve the precipitation for the month of June
june_prcp = session.query(Measurement).filter(extract('month', Measurement.date) == 6)

# Perform a query to retrieve the precipitation for the month of December
december_prcp = session.query(Measurement).filter(extract('month', Measurement.date) == 12)

