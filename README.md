# WeatherPy Project

# Part 1 - Analysis of weather data across cities worldwide 

## Overview
WeatherPy is a comprehensive Python project designed to analyze weather data across a diverse set of cities worldwide. The project integrates with the OpenWeatherMap API to gather real-time weather information, encompassing temperature, humidity, cloudiness, and wind speed. The data is meticulously analyzed and visualized using scatter plots and linear regression to illustrate the relationship between these weather variables and latitude.

## Dependencies and Setup

To run the WeatherPy project successfully, ensure you have the following Python libraries installed:
* matplotlib.pyplot: Used for generating plots and visualizations.
* pandas: Essential for data manipulation, cleaning, and analysis.
* numpy: Provides support for numerical operations and computations.
* requests: Enables HTTP requests to retrieve data from the OpenWeatherMap API.
* scipy.stats: Offers statistical functions necessary for data analysis.
* citipy: Utilized to identify the nearest city based on latitude and longitude coordinates.
* api_keys: A custom module to store the OpenWeatherMap API key securely.

## Data Generation

### Generate the Cities List
The project begins by creating a list of cities using randomly generated latitude and longitude coordinates. The latitude ranges from -90 to 90, and the longitude ranges from -180 to 180. The citipy library is then employed to determine the nearest city for each coordinate pair. This process ensures a diverse set of global cities for comprehensive weather analysis.

## Data Retrieval and Analysis

### Fetch Weather Data
Weather data for each city in the generated list is fetched from the OpenWeatherMap API. The data retrieved includes latitude, longitude, maximum temperature, humidity, cloudiness, wind speed, country, and date. This data is organized into a structured format using Pandas DataFrame, facilitating easy manipulation and analysis.

### Scatter Plots
The project includes four distinct scatter plots, each showcasing the relationship between latitude and a specific weather variable:
1. Max Temperature: Highlights the temperature variations across different latitudes.
2. Humidity: Depicts the distribution of humidity levels across latitudes.
3. Cloudiness: Illustrates the cloud cover percentage relative to latitude.
4. Wind Speed: Displays the wind speed variations based on latitude.

These visualizations offer valuable insights into how weather conditions evolve across different geographical locations.

### Linear Regression Analysis
To further understand the relationship between latitude and the weather variables, linear regression analysis is conducted for both the Northern and Southern Hemispheres. Each scatter plot is accompanied by a regression line, providing a clear visual representation of the correlation. The r-value is also calculated and displayed to quantify the strength of the relationship.

## Conclusion
WeatherPy serves as an insightful tool for analyzing global weather patterns and trends. By leveraging real-time data and advanced analytical techniques, the project offers a nuanced understanding of how various weather variables are influenced by geographical location. Whether for academic research, business planning, or personal interest, WeatherPy provides a robust platform for exploring and interpreting weather data on a global scale.

# Part 2 - Creating Interactive Map for identifying ideal vaction spots 

## Overview
VacationPy is a Python project designed to assist users in identifying ideal vacation spots based on specific weather criteria. Leveraging the WeatherPy project's output data, VacationPy utilizes geographic and weather information to generate an interactive map displaying potential vacation destinations. The map highlights cities that meet the user-defined weather conditions, along with the nearest hotel within a 10,000-meter radius.

## Dependencies and Setup

Ensure you have the following Python libraries installed to execute VacationPy:
* hvplot.pandas: Used for creating interactive visualizations.
* pandas: Required for data manipulation and analysis.
* requests: Enables HTTP requests to retrieve data from the Geoapify API.
* api_keys: A custom module to securely store the Geoapify API key.

## Data Loading and Preparation

### Load Weather Data
The project starts by loading the CSV file generated from WeatherPy into a Pandas DataFrame. This dataset contains comprehensive weather information for various cities worldwide, including latitude, longitude, maximum temperature, humidity, cloudiness, and more.

### Create Interactive Map
An interactive map is generated using the hvplot library to plot each city from the dataset. The size of each point on the map corresponds to the humidity level of the respective city, providing a visual representation of humidity variations across different locations.

## Ideal Vacation Spot Selection

### Narrow Down Cities
The dataset is filtered to identify cities that match the ideal weather conditions specified by the user. In this case, cities with a maximum temperature below 25°C and cloudiness less than 25% are considered.

### Create Hotel DataFrame
A new DataFrame named hotel_df is created to store essential information about the selected cities, including city name, country, coordinates, and humidity level. An additional empty column, "Hotel Name," is added to store the name of the nearest hotel.

### Find Nearest Hotels
For each city in hotel_df, the Geoapify API is utilized to search for the nearest hotel within a 10,000-meter radius. The hotel name is retrieved and stored in the "Hotel Name" column. If no hotel is found within the specified radius, "No hotel found" is set as the value.

## Interactive Map with Hotel Information

### Update Map with Hotel Data
The interactive map is updated to display the selected cities along with the nearest hotel and country information. Hovering over each city point on the map will provide a tooltip with the hotel name and country, aiding users in making informed decisions about their vacation destinations.

## Conclusion
VacationPy offers a user-friendly and interactive platform to discover potential vacation spots based on personalized weather preferences. By combining weather data with hotel information, the project simplifies the vacation planning process, allowing users to explore and select the perfect getaway locations effortlessly. Whether you're seeking a sunny beach destination or a cozy mountain retreat, VacationPy provides the tools to find your ideal vacation spot with ease.

## WeatherPy Repo Structure: 
* WeatherPy.ipynb: analysis the weather data across a diverse set of cities and worldwide
* VacationPy.ipynb: code for assisting users in identifying ideal vacation spots based on specific weather criteria.
* Output_data: illustrations from the data analysis from weather data 


