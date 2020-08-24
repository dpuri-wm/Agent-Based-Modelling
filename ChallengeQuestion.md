# Challenge Question

In this assignment, I created a plot on RStudio with 50 randomly placed dwelling uits, 40 small trees (represented by the small, bright green circles), and 12 large trees (represented by the large green/beige circles). Next, I randomly selected 7 homes from the 50, and used a dash line to represent a person's path between the homes! Below is my plot and the script I used to produce it. 

![Screen Shot 2020-08-23 at 7 52 19 PM](https://user-images.githubusercontent.com/60228374/90991994-f193fd80-e57a-11ea-899d-8b6e921591ee.png)
![Screen Shot 2020-08-23 at 7 52 39 PM](https://user-images.githubusercontent.com/60228374/90991995-f5278480-e57a-11ea-9ba4-06d8f0b11006.png)

Through this assingment, I learned how to produce basic code in R. 


- To create an object, and assign it a value, use "<-" 
  - x <- 1:10
  - X would be "holding" : 1 2 3 4 5 6 7 8 9 10
- To make a simple plot, simply say "plot(x,y)"
- To add circles of the points on the plot: "plot(x, y, type = "o")"
- To add a title, use the function "main"
  - plot(x, y, type = "o", 
    main = "The Path of a Running Boy",
    sub = "units of distance = meters",
    xlab = "longitude", 
    ylab = "latitude")
- The command "sample" will randomly select numbers in a uniform manner
  - east <- sample(x, size = 10, replace = TRUE)
  - use "replace =" and write true or false, depending if you want values to be repeated
- To create a dataframe
  - dwellings <- cbind.data.frame(id = 1:10, east, north)
  
  
  
