---
title: "Beer Analysis Codebook"
author: "Bodie Franklin, Ellen Lull"
date: "3/7/2020"
---

## Project Description
The goal of this project was to analyze data on 2410 craft beers created in 558 breweries across the United States to determine any additional  opportunities for Budweiser.  Data collected included alcohol by Volume (ABV), International Bitterness Units (IBU) and the Style of each craft beer.  


##Creating the tidy datafile

###Guide to create the tidy data file
1. Downloaded Beers.csv and Breweries.csv
2. Merged datasets into one dataset
3. Imputed missing data for ABV.   This was done by averaging the ABV values by beer style
4. Imputed missing data for IBU.   This was done by calculating and averaging the Alpha Acid * Boil Time by Beer Style and imputing IBU Values based on this average
5. Removed 52 rows of styles such as cider which did not have enough IBU data to calculate an average


###Cleaning of the data
1. Imputed missing data for ABV.   This was done by averaging the ABV values by beer style
2. Imputed missing data for IBU.   This was done by calculating and averaging the Alpha Acid * Boil Time by Beer Style and imputing IBU Values based on this average
3. Removed 52 rows of styles such as cider which did not have enough IBU data to calculate an average


###  Variables
Beers.csv:
Name: Name of the beer
Beer_ID: Unique identifier of the beer
ABV: Alcohol by volume of the beer
IBU: International Bitterness Units of the beer
Brewery_ID: Brewery id associated with the beer
Style: Style of the beer
Ounces: Ounces of beer

Breweries.csv:
Brew_ID: Unique identifier of the brewery.
Name: Name of the brewery.
City: City where the brewery is located.
State: U.S. State where the brewery is located.

Combined Final dataset:
Brewery_ID: Brewery id associated with the beer
Beer_name: Name of the beer
Beer_ID: Unique identifier of the beer
Ounces: Ounces of beer
 
drvABV: Derived Alcohol by Volume   Missing values filled in by averaging ABV by style

drvIBU: Derived International Bitterness Units.  Missing values filled in by calculating and averaging the Alpha Acid * Boil Time by Beer Style and imputing IBU Values based on this average

Brewery_name: Name of the brewery.
City: City where the brewery is located.
State: U.S. State where the brewery is located.
Type:  Type of beer classified as Ale or IPA based on beer style
