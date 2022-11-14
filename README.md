# WeatherPy with Python APIs

## Purpose of the analysis
Weather Analysis performed to random cities around the globe in order to present a list of options to the user and create a travel plan using Google Maps Platform

## Analysis

### Retrieve Weather Data
From 2,000 random locations we selected the same number of valid cities using citipy module to get the nearest city for each latitude and longitude combination, then using the OpenWeatherMap's API service we retrieve the following information from the API call:
  Latitude and longitude
  Maximum temperature
  Percent humidity
  Percent cloudiness
  Wind speed
  Weather description (for example, clouds, fog, light rain, clear sky)
 Finally we convert all json responses to a DataFrame using the Pandas function and save it as txt file.
 
### Create a Customer Travel Destinations Map
We filter only the cities that met the criteria using a range of temperatures that the user input on the sequence as maximum and minimum temperature that they prefer.
From the filtered list we retrieve the nearest hotel based on the search parameters provided using the Google Map service and the latitude and longitude of each city, then we added the hotel name to the hotel_df DataFrame and dropped any rows in the hotel_df DataFrame where a hotel name is not found.

### Create a Travel Itinerary Map
Finally, we select four cities close to each other to plan a trip using adding a directions layer map between the cities using the Google Maps service.
