

---

## Part 1: WeatherPy

The **WeatherPy** script will visualize weather data for over 500 cities at varying distances from the equator.

### Steps:

1. **Generate random geographic coordinates**: 
   - Randomly generate latitude and longitude values.
   - Use the `citipy` Python library to find the nearest city to each coordinate.

2. **Retrieve weather data**: 
   - Use the OpenWeatherMap API to collect weather information for each city.

3. **Create scatter plots** to display the following relationships:
   - Latitude vs. Temperature
   - Latitude vs. Humidity
   - Latitude vs. Cloudiness
   - Latitude vs. Wind Speed

4. **Northern and Southern Hemisphere Analysis**:
   - Separate the plots by hemisphere (Northern and Southern).
   - Perform a linear regression analysis to assess how weather changes based on proximity to the equator.

The linear regression will help demonstrate whether weather conditions vary with distance from the equator.

---

## Part 2: VacationPy

**VacationPy** will show how weather data can be leveraged for vacation planning using the Geoapify API and the `geoViews` Python library.

### Steps:

1. **Create a map of cities**:
   - Use the `city_data_df` DataFrame (containing weather data from WeatherPy).
   - Display a point for each city, with the size of the point representing humidity levels.

2. **Filter cities for ideal weather conditions**:
   - Narrow down cities based on specific criteria, for example:
     - Max temperature between 21°C and 27°C
     - Wind speed less than 4.5 m/s
     - No cloudiness
   - Aim to limit the filtered cities to 10-20.

3. **Create a `hotel_df` DataFrame**:
   - Store city, country, coordinates, and humidity information.
   - Use the Geoapify API to find the nearest hotel within 10,000 meters of each city's coordinates.
   - Include the hotel name and country in the hover messages on the map.

### User Guide:

1. **WeatherPy.ipynb**:
   - Run this notebook to collect and store weather data from 550-650 cities globally using randomly generated coordinates.
   - API keys for Geoapify and OpenWeatherMap will be required.
   - Graphs and charts created by WeatherPy will be saved in the `output_data` folder.

2. **VacationPy.ipynb**:
   - Run after WeatherPy.ipynb (dependent on its data).
   - Use it to plan vacations based on weather data and visualize the results on a map with relevant hotel information.

---

