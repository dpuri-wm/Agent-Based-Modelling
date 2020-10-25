# PROJECT 2 DELIVERABLE
## Ethiopia, Africa

A) In order to obtain the DHS data, I submitted a request for access to the Ethiopia 2016 Households and Persons survey dataset. In my explanation, I stated that I intended to use the data to generate a synthetic population that I could use in my agent-based model. Furthermore, I needed the remotely sensed data to estimate dwelling locations and other features of the data.

   The DHS (Demographic and Health surveys) data is for Ethopia in 2016. In my source data, 16,500 households were sampled with 15,683 females surveyed and 12,688 males surveyed. The variables we were most interested in studying were: sex, age, education, and wealth. Something I found interesting when I was reading about the data was that men had a lower response rate than women, when it came to interviews. However, rural men had a higher response rate than men in urban locations. I pulled the age and sex of household members, region identifier (location), and sample weights. In general, this step was not too complicated as it just involved reading in the data, and finding the columns that corresponded to the variable I wanted to extract. 

B) I faced major computational limitations when spatially locating households at the adm 0 level. There were 16650 households, and it took a while for my laptop to locate households based on population density of Ethiopia (I go into more depth at the adm 2 level). I received a person-level error of 2.17%. 

C) I began spatially locating my households at the Adm 2 level. I chose Afar Regional state, an adm 2 region, to focus on. The population of Afar is roughly 1.8 million people, and I was especially interested in choosing this specific location since in project 1, I studied Eritrea. The region of Afar is the location of regional instability between Ethiopia and Eritrea. Essentially, in order to locate my households, I used the spatstat::rpoint() command and found hhs_pts and hhs_locs after extracting population density from a 2016 population raster of Ethopia. Here is my density plot for one of the households at the adm 2 level:

![afar1](https://user-images.githubusercontent.com/60228374/97117299-1cb0df80-16d9-11eb-9850-93d9f27f8dc6.png)

I calculated the person level error at the adm 2 level to be 2.24%. Percent error at the adm 0 level is much more accurate than at the adm 2 level, since the survey was designed at the country level. Also, it's easier to know exactly how many households are in a district, but it's more difficult to know how many persons are in the household. Some of the error definitley stemmed from the creation of the pns, from the household survey. Below, I included my code to create the pns which involved pivoting gender, age, and education. I did this through creating pivot objects, going through my hhs dataframe,finding the column numbers that aligned with the variable I was interested in. Next, I looked at where gender and pnmbr were and created the pns dataframe that included the pivot objects of gender, age, and education. My pns did not 100% match my summing of weights that come from household observations; they were slightly less (75122 < 78064). Steps could be taken to increase the level of accuracy. One of the strecth goals was to use GPS data instead of the whole country to locate households. This would have helped immensely as we would have been able to locate households within a 2-5 km radius. Lastly, subsetting the sample made the locations at the adm 2 level less accurate. Sample size is quite small when subsetting; it is not enough to represent the entire district. Ideally, we would subset not only to Afar, but to nearby regions as well.




D) My synthetic population, afar_synpop, definitly is a better representation of the demographic features of households and persons, compared to any randomly generated synthetic population. For one, I took measures to prepare the synthetic population data. I understood, for example, that when predicting gender based off age, for example, the relationship would be very heavily skewed. This is because age can take on a variety of values(4 y/o, 28 y/o, 67 y/o). Meanwhile, gender can only be one of two values (0 or 1). The resulting relationship would be very skewed, so in order to fix this, I scaled the data. I plotted heatmaps to help visualize the data after scaling, normalizing, and and percentizing. Here are the plots (first plot is before taking any measures). 


![rawE](https://user-images.githubusercontent.com/60228374/97117222-a3b18800-16d8-11eb-8e51-51fca1d5c512.png)
![scale](https://user-images.githubusercontent.com/60228374/97117223-a613e200-16d8-11eb-80af-f879539b124b.png)
![normal](https://user-images.githubusercontent.com/60228374/97117224-a7dda580-16d8-11eb-811c-74748dd92be6.png)
![percent](https://user-images.githubusercontent.com/60228374/97117228-aad89600-16d8-11eb-9c3e-2df5de5a2919.png)


Lastly, I used tidymodels, keras, and random forest to model my synthetic population for Afar. However, my greatest accuracy was ~ 16 %. This accuracy is definitley very low, but still better than a randomyl generated synthetic population. Furthermore, it provides evidence that a more accurate synthetic population could be achieved. 


