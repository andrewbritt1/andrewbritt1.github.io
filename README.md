
This project outlines a process to identify the top 20 areas by zipcode to start a breakfast restaurant in the Dallas-Fort Worth metroplex using existing crime, population and restaurant data
For success criteria, we've identified the following elements that will be used to generate a top down score by zipcode -
- the highest population
- highest safety (low crime)
- lowest competition


To start, we need to find city and zipcode data. This can be found from the following source - https://simplemaps.com/data/us-zips. This data will be in csv format and imported as a dataframe for as we go through this exercise. Luckily this data source also includes population by zipcode as part of the data set.

Since our client would like a map with results, we will need to gather geo location data that will enable us to display data by zipcode. This can be found from the following source - https://github.com/OpenDataDE/State-zip-code-GeoJSON/blob/master/tx_texas_zip_codes_geo.min.json. We will ultimately use this json to create a choropleth heat map by zipcode.

The client needs to know what competition they could face at their location of choice. Thus, we need to pull a breakfast restaurant count by zipcode that will be integrated into the zipcode score. We will use the foursquare API to capture this data into a dataframe.

Lastly, we identified that safety and/or crime is important to business owners and their customers. We will pull this data from https://www.bestplaces.net. This website will provide a violent crime and property crime rank on a scale of 1 to 100 by zipcode. To pull this data, we require Selenium Webdriver to loop through through the website using our zip code data to pull crime statistics.


Data Sources:

- city, zipcode and population source - https://simplemaps.com/data/us-zips
- zip code geo data source - https://github.com/OpenDataDE/State-zip-code-GeoJSON/blob/master/tx_texas_zip_codes_geo.min.json
- competition source - https://foursquare.com/
- Crime rating data source - https://www.bestplaces.net

- Follow the link below for the process and results

[ DFW - Top 20 Areas by Zipcode](https://nbviewer.org/github/sp1ral0u1/sp1ral0u1.github.io/blob/main/Restaurant%20Startup%20Location%20Ranking%20By%20Zipcode%20-%20Final%20Version%20%28for%20repo%29.ipynb)

<iframe src="https://nbviewer.org/github/andrewbritt1/andrewbritt1.github.io/blob/24700fb3ba8411465d8053f3e9764c92cb919687/Restaurant%20Startup%20Location%20Ranking%20By%20Zipcode%20-%20Reduced.ipynb" width="100%" height="500"></iframe>
