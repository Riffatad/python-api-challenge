# python-api-challenge.
# WeatherPy:
This code is designed to analyze and visualize weather data for cities around the world using the OpenWeatherMap API.
The process begins by importing necessary libraries such as Matplotlib, Pandas, NumPy, and SciPy for data manipulation and visualization. It also utilizes the Citipy library to find the nearest cities based on random latitude and longitude coordinates generated within valid ranges.
Key Steps in the Code:
Data Retrieval:
The code generates 1,500 random latitude and longitude pairs. For each pair, it identifies the nearest city using the Citipy library and collects unique city names.
It then constructs API requests to the OpenWeatherMap service to fetch weather data (maximum temperature, humidity, cloudiness, wind speed, country, and date) for each city.
Data Storage:

The retrieved weather data is compiled into a Pandas DataFrame, allowing for easy manipulation and analysis.
Data Visualization:

Several scatter plots are created to explore relationships between latitude and different weather variables:
Latitude vs. Maximum Temperature
Latitude vs. Humidity
Latitude vs. Cloudiness
Latitude vs. Wind Speed
Each plot includes titles, axis labels, and grid lines for clarity. The plots are saved as PNG files.
Linear Regression Analysis:

For both the Northern Hemisphere (latitude ≥ 0) and Southern Hemisphere (latitude < 0), the code creates separate DataFrames.
It performs linear regression to analyze the relationship between latitude and each weather variable. The regression equation and R² value are calculated and displayed on the plots to indicate the strength of the correlation.
Final Output:

The results include visualizations that showcase how latitude influences various weather metrics, helping to identify trends or anomalies across different geographical regions.
Overall, this code provides a comprehensive approach to gathering, analyzing, and visualizing global weather data, enabling further exploration of climate patterns and trends based on geographic location.

# Vacation Py:

VacationPy
Overview
VacationPy is a project that leverages the Geoapify API to visualize geospatial data and find hotels based on specific weather conditions. The goal is to help users identify cities with ideal weather and provide nearby hotel options.

Getting Started
To begin, you will need to install a few Python packages, including hvplot, pandas, requests, and json. You can easily install these dependencies using pip:

bash
Copy code
pip install hvplot pandas requests
API Key

Before running the project, clone the repository to your local machine. You will also need an API key from Geoapify. Store this key in a file named api_keys.py located in the same directory as your main script. The key is used to authenticate requests to the Geoapify API.

Import Libraries: Start by importing the necessary libraries in your Python script.

Load Data: The project loads a CSV file containing city data into a Pandas DataFrame, allowing you to explore its structure and contents.

Visualize Data: You can create a map that plots points for each city, with sizes representing humidity levels. This visual representation helps you quickly assess the weather conditions across different locations.

Filter Cities: The DataFrame can be filtered to find cities that meet your ideal weather criteria, such as specific humidity and temperature ranges.

Fetch Hotel Data: Once you have identified suitable cities, the project will create a new DataFrame to store information about hotels in these locations. It uses the Geoapify API to search for the first hotel located within 10,000 meters of each city’s coordinates.

An example of fetching and visualizing data from the Geoapify API is included in the project. This example will guide you through the process of obtaining geospatial data and displaying it effectively.
