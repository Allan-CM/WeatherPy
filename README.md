# WeatherPy Project

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

## Linear Regression Analysis
To further understand the relationship between latitude and the weather variables, linear regression analysis is conducted for both the Northern and Southern Hemispheres. Each scatter plot is accompanied by a regression line, providing a clear visual representation of the correlation. The r-value is also calculated and displayed to quantify the strength of the relationship.

## Conclusion
WeatherPy serves as an insightful tool for analyzing global weather patterns and trends. By leveraging real-time data and advanced analytical techniques, the project offers a nuanced understanding of how various weather variables are influenced by geographical location. Whether for academic research, business planning, or personal interest, WeatherPy provides a robust platform for exploring and interpreting weather data on a global scale.
