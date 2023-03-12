### *Start A Restaurant! Where do I go?*

This project outlines a process to identify the top 20 areas by zipcode to start a breakfast restaurant in the Dallas-Fort Worth metroplex using existing crime, population and restaurant data
For success criteria, we've identified the following elements that will be used to generate a top down score by zipcode -
- the highest population growth over time
- highest safety (low crime)
- lowest competition

To start, we need to pull city and zipcode data. This can be found here - [US zip code information](https://simplemaps.com/data/us-zips). This data will be in csv format and imported as a dataframe for as we go through this exercise. Luckily this data source also includes population by zipcode as part of the data set.

Next, we will need to gather geo location data that will enable us to display data by zipcode. This can be found here - [Texas zip code Geo information](https://github.com/OpenDataDE/State-zip-code-GeoJSON/blob/master/tx_texas_zip_codes_geo.min.json). We will ultimately use this json to create a choropleth heat map by zipcode.

We need to know what competition near the location of choice. Thus, we need to pull a breakfast restaurant count by zipcode that will be integrated into the zipcode score. We will use the foursquare API to capture this data into a dataframe.

Lastly, we identified that safety and/or crime is important to business owners and their customers. This can be pulled from [bestplaces.net](https://www.bestplaces.net). This website will provide a violent crime and property crime rank on a scale of 1 to 100 by zipcode. To pull this data, we require Selenium Webdriver to loop through through the website using our zip code data to pull crime statistics.


Data Sources:

- city, zipcode and population source - https://simplemaps.com/data/us-zips
- zip code geo data source - https://github.com/OpenDataDE/State-zip-code-GeoJSON/blob/master/tx_texas_zip_codes_geo.min.json
- competition source - https://foursquare.com/
- Crime rating data source - https://www.bestplaces.net

Follow the links below for the process and results:

[ DFW - Top 20 Areas by Zipcode (nbviewer)](https://nbviewer.org/github/andrewbritt1/andrewbritt1.github.io/blob/108eb86ca5297eaaac004ce0b2eb4daaa70d2f96/Restaurant%20Startup%20Location%20Ranking%20By%20Zipcode%20-%20Final%20Version%20%28for%20repo%29.ipynb) | [ DFW - Top 20 Areas by Zipcode (github)](https://github.com/andrewbritt1/andrewbritt1.github.io/blob/108eb86ca5297eaaac004ce0b2eb4daaa70d2f96/Restaurant%20Startup%20Location%20Ranking%20By%20Zipcode%20-%20Final%20Version%20(for%20repo).ipynb)

<iframe src="https://nbviewer.org/github/andrewbritt1/andrewbritt1.github.io/blob/909f82d58a6d738c4788de8b1e1a7b8a03626f90/Restaurant%20Startup%20Location%20Ranking%20By%20Zipcode%20-%20Reduced.ipynb" width="100%" height="500"></iframe>
