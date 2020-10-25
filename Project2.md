## The DATA
To obtain the following data, I submitted a request for access to the Ethiopia 2016 DHS dataset. Below is my request:

I would like to improve upon the use of multinomial logistic regression models to generate a close-to-reality
synthetic population in Ethiopia. I'm interested in using an agent-based model to learn more about human
behavior in Ethiopia, specifically in Tigray since it's on the border of Eritrea. The data would help me to create
a synthetic population I can utilize in my model. Specifically, the remotely sensed data would allow me to
estimate dwelling locations , and other data would help me estimate size/gender.other features of the
population. Additionally, I'm
interested in studying the intersection of human behavior, interactions, infrastructure, and overall health in
the country. Thank you.

### A little about the data
- The DHS Survey data is for Ethiopia in 2016
- Data was collected between January 2016 and June 2016
- 16,650 households were sampled, with 15,683 females surveyed, and 12,688 males
- In 2016, Total ethiopia population was 103.6 million persons

### Afar, Ethiopia

Afar Regional State is a region in my adm_1 that I decided to zoom in on! It has a population of ~ 1.8 million persons. This region has been the location of major instability due to the Ethiopian - Eritrean war of 1998-2000. The area is heaily agricultural. Below shows the population:

![Screen Shot 2020-10-18 at 6 04 12 PM](https://user-images.githubusercontent.com/60228374/96386967-ef11e680-116c-11eb-9e67-b4e2762b96c9.png)



### Addis Abeba, Ethiopia

Due to some laptop constraints and other plotting issues, I was only able to plot the households across the Addis Abeba region. Addis Abeba is the captial of Ethiopia, and below is my planar point pattern:

![Screen Shot 2020-10-18 at 6 10 57 PM](https://user-images.githubusercontent.com/60228374/96387064-85460c80-116d-11eb-9a1f-474a4c3cf548.png)

I have also included the population plot:

![Screen Shot 2020-10-12 at 1 41 55 PM](https://user-images.githubusercontent.com/60228374/96387220-685e0900-116e-11eb-86b2-18235563a355.png)

Originally, I had intended to work with Addis Abeba, but the population size was too large, and my latop was not able to generate households from the adm1 data, when I had filtered it to Addis Abeba.

### Density Plot
Density plot of the sampled household in Afar.

![afar1](https://user-images.githubusercontent.com/60228374/97117531-b9c04800-16da-11eb-81a5-8d16b1a5b2db.png)


### Conclusion

My final training model accuracy ~ 16%.  This project was definitly chanllenging in many ways. Aside from having trouble keeping my script organized and clean and avoiding language errors (kept using some python syntax), I learned  a lot. One of the most important things i learned in this project was how to pivot the age, gender, and education variables. I did this through creating pivot objects from going into my af_hhs dataframe and finding the column numbers that aligned with the variable I was interested in. Next, I looked at where gender and pnmbr were and created the pns dataframe that included the pivot objects of gender, age, and education. Another skill I definitly brushed up was binding/merging dataframes, and splicing them. I became familiar with how to generate randomly sampled households, and calculating average household size. In general, I enjoyed this project.


