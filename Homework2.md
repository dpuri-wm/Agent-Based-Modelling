## Extracting populations from a Raster and Aggregating to each Unit

In this assignment, I selected to produce the geospatial data plots of the LMIC, Lesotho. Lesotho is a land-locked country, located in Southern Africa. Lesotho's capital is Maseru, and its 2019 population is 2,125,268 persons. I began by downloading Lesotho's 2019 population data from the World pop website. Throughout the assignment, I used the raster package in RStudio to create a raster layer. I was able to plot the first administrative level with the raster layer on top of it. At the end of the assignment, I was able to actually "add" this raster layer to my variable, lso_adm1, which had all the adminsitrative boundary information. I separated population counts based on their "ID", which just meant which administrative district. When I summed all the population counts, I got a total population of : 1,855,656. This value is definitly a little off, but still is close. Below are some fun pictures of some of the plots and dataframes I produced:

![Screen Shot 2020-08-27 at 4 25 49 PM](https://user-images.githubusercontent.com/60228374/91494981-c44f9400-e887-11ea-8158-d442626dfe00.png)
![Screen Shot 2020-08-27 at 4 41 50 PM](https://user-images.githubusercontent.com/60228374/91494988-c6b1ee00-e887-11ea-806d-753d2935f891.png)
![Screen Shot 2020-08-27 at 4 58 23 PM](https://user-images.githubusercontent.com/60228374/91494990-c9144800-e887-11ea-82c4-7f81c815dc70.png)
![Screen Shot 2020-08-27 at 4 53 12 PM](https://user-images.githubusercontent.com/60228374/91494996-cade0b80-e887-11ea-8a11-c439ac603288.png)

It's really interesting because you can see in the third plot that Maseru is in red, meaning it has a very high population! This is accurate as that is the capital, and thus many people must live there to be in an urban setting. 
