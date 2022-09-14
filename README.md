In this activity, I'll take the weather data of 500+ randomly selected cities around the world then analyse the data to see any relations between cities lat/lon and its weather.

Here is how I approached the problem:
- Firstly, I generated 500+ random lat/lon data
- Used citipy to find the nearest city to those lat/lon
- Then, I connect to the weather API (https://api.openweathermap.org/data/2.5/weather) to take the weather data of those cities
- The last step is to use Pandas to prepare the data and visualise it

Below are some findings:

There is **a strong correlation between latitude and temperature**. The higher the latitude (either North or South) and lower the temperature.

![alt text](WeatherPy/output_data/Fig1.png)


There is no correlation between latitude and other weather parameters.

![alt text](WeatherPy/output_data/Fig2.png)

![alt text](WeatherPy/output_data/Fig3.png)

![alt text](WeatherPy/output_data/Fig4.png)


To make this a bit more interesting, I created a heat map that displays the humidity for every city above. Then narrowed down the DataFrame to find cities with the ideal weather condition. For example:
- A max temperature lower than 25 degrees but higher than 15.
- Wind speed less than 10 mph.
- Zero cloudiness.
After that, I used Google Places API to find the first hotel for each city within 5000 meters of my coordinates. Finally, I plotted the hotels on top of the humidity heatmap with each pin containing the Hotel Name, City, and Country.


![alt text](WeatherPy/output_data/heat_map_with_hotel_marker_layer.png)

Voila, I now have a map of current cities with ideal weather and the nearest hotel. If I have money, I can go there and enjoy the weather immediately (just wishing...).
