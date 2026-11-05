# Travel Packing Assistant — Proposal

## What I am building
I want to build a travel packing assistant that uses real weather forecasts to help people decide what to bring on their trips.

## Who it is for
This tool is for travelers like me who sometimes struggle to decide what clothes and essentials to pack, especially when visiting places with unfamiliar weather.

## The API
I will use the Open-Meteo Weather API.

Documentation: https://open-meteo.com/en/docs

Example URL I tested:
https://api.open-meteo.com/v1/forecast?latitude=51.5085&longitude=-0.1257&daily=temperature_2m_max,temperature_2m_min,precipitation_probability_max,weather_code&timezone=Europe%2FLondon&forecast_days=3

The fields I plan to use are `time`, `temperature_2m_max`, `temperature_2m_min`, `precipitation_probability_max`, and `weather_code`.

## What the user chooses
The user will choose a destination and travel dates within the available forecast period.

## What the page works out
The website will analyze the forecast and recommend clothing and other essentials based on the expected temperature, rain, and weather conditions.

## Features
1. Search for a travel destination.
2. Choose travel dates.
3. Display the weather forecast.
4. Generate a personalized packing checklist.
5. Check off items as they are packed.

## What I do not know yet
I need to learn how to connect a destination search to the weather API, use JavaScript to read the returned data, calculate packing recommendations, and display those recommendations on the page.