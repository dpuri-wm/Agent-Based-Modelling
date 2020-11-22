
From the Garcia et. al paper, we learned the importance and benefits of utilizing gravity models when analyzing human migration. To begin project 3, we began by creating a gravity model for London - following a guide by Dr Ds. Essentially, we did this by calculating a distance matrix between boroughs in London, and using transport data for migration flow estimates. Utilizing the gravity model allowed us to look at flow estimates, and original flows. 



### Origin-Destination (OD) Matrix 

![Screen Shot 2020-11-19 at 1 59 22 PM](https://user-images.githubusercontent.com/60228374/99711229-88cffa80-2a6f-11eb-8871-fc9f86775c19.png)

This is a snippet to reveal what my OD matrix looked like. I downloaded data on internal migration flows in ethiopia, from the worldpop.data website. Next, I found the origin flows sum and destination flows sum for each adminsitrative 1 district in Ethiopia. Using these sums, I was able to create the OD matrix to have a better visualization of people migrarting between the districts. The N/A is inter-migration within districts, which wasn't calculated. 

### Animated Migration

I used the OD matrix to create an animation of migration within Ethiopia. 

![output](https://user-images.githubusercontent.com/60228374/99711899-58d52700-2a70-11eb-9236-48c97e181717.gif)

### Tesselation of Voronoi Polygons

Below is the voronoi polygons produced for the municipalities of Afar Zone 4, within Afar, within Ethiopia, Africa. Similar to how we created an origin/destination matrix in the London gravity model exercise, if I wanted to produce an OD matrix at these higher resolution entities, I would narrow down the data from the worldpop.org that was used to make the ABM of migration flow in Ethiopia. The voronoi projection defines the centerpoints, and to better model migration flow, I would probably modify the number of points departing from each origin. I think it would be a really good idea to incorporate transportation vehicles, as thats a better representation of what's going on in reality. 

![Screen Shot 2020-11-19 at 12 14 06 PM](https://user-images.githubusercontent.com/60228374/99712456-152eed00-2a71-11eb-90b9-7a609f64d14f.png)

### Urbanized areas within Afar
![afar_v1](https://user-images.githubusercontent.com/60228374/99712887-a8682280-2a71-11eb-971b-cac830904d74.png)
