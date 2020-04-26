# IBM Data Science Capstone Project

# Texas Derby, Austin, Dallas or Houston?
## Introduction / Scope

**Austin, Dallas, and Houston** are the three major cities in the great state of Texas. In the past decades, these three cities have experienced rapid population growth amid Texas’s progressing economy. **Austin**, being the capital of the Lonestar State with an eclectic mix of history, culture, and gorgeous sights, has also emerged as a technology hub. Austin’s Silicone Hill is considered a substitute for the Bay Area’s Silicon Valley. **Dallas**, together with its rapidly growing twin city of Fort Worth and other satellite cities in the vicinity, stands as a multi-versed financial and technology center at the Southwest. **Houston** has always been the energy center in America. It’s energy, engineering, petrochemical, and other industries have empowered this city with a robust lifestyle.

**Texas** has been consistently ranked number one for the inflow of migrants from other states across America due to employment opportunities and relatively low living cost. While most of the people inflow will settle down in one of the three cities abovementioned, the cities themselves have a lot of things to offer and explore. **This analysis intends to show which areas (by Zip Code) of a town resemble those of the others.(Austin, Dallas, Houston).** 

### This report could be helpful for different use cases:

•	**People moving from one city to the other** often would like to live in a particular type of neighborhood. This comparison can help those to filter for areas similar (or even different, if you are up for something new) to what you are used to.

•	**People moving from other states to Texas** often wonder where to settle down. This comparison can help those to filter for neighborhoods similar or different from their original came from, and introduce them into local fun and popular places.

•	**Companies expanding within one of the cities** might want to look for a similar type of neighborhoods, as they are targeting a specific user group. The comparison can offer the first indication.

•	**Companies expanding from one city to the other** might also try to find a neighborhood to settle in first. They can use their experience from the original city and look for a fitting (e.g., similar) neighborhood in the second one.

## Data Collection
#### Two different kinds of data are used for this comparison.

**1. City zipcode area and corresponding geographical data**:  to analyze the cities on a meaningful level, they need to be divided into different areas, e.g., neighborhoods, boroughs, or simply by **zip codes**. Luckily the zipcode data is readily available on the internet, and one can be found [here](https://simplemaps.com/data/us-zips). 

This data (uszip.csv), when unzipping, includes 33099 rows of almost **all zip codes across the USA**. It also consists of latitude and longitude coordinates for each zip code, which will be useful later when it comes to geo-location analysis using FourSquare API. Other relevant information, such as corresponding city, county, population, etc. are also included in the dataset. Some cleaning and filtering of data need to be done first in order to **limit the analysis to Texas**, and more specifically, to the **three cities mentioned**.  

When we talk about a city, we often refer to the **metropolis** together with its adjacent areas. For example, when we talk about Dallas, it doesn’t only include the city of Dallas, but also include the city of Fort Worth, Plano, Frisco, Denton, etc.. The same principle applies to Austin (The greater Austin Area) and Houston (The greater Houston Area). One way to achieve this is to **include county data**. For example, the city of Dallas is in Dallas County, but the whole Dallas-Forth Worth (DFW) area will consist of 4 counties, i.e., Dallas, Collin, Tarrant, and Denton. So **county data** and **zipcode data** will be used for geo-location.

**2. Venue data**: The first 500 venues per ZIP-code in **Austin (AUS), Dallas (DFW), and Houston (HOU)** are scraped from the **FourSquare API**,  in order to cluster according to the zip and county boundaries. Because the zipcode data also contains latitudes and longitudes, the **coodinates** are used to match the venue data and extract information about the Venue name, category, locations using the Foursquare API.

Other standard applications and analysis of the datasets are referred to the vaious IBM Coursera Course Labs.












