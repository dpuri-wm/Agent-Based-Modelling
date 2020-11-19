
### Origin-Destination (OD) Matrix 

odm <- pivot_wider(data = flows, id_cols = NODEI, names_from = NODEJ, values_from = PrdMIG)

odm <- odm[ ,-1]

odm <- odm[ ,c(16,2:15)]

![Screen Shot 2020-11-19 at 1 59 22 PM](https://user-images.githubusercontent.com/60228374/99711229-88cffa80-2a6f-11eb-8871-fc9f86775c19.png)

This is a snippet to reveal what my OD matrix looked like. 

### Animated Migration

![output](https://user-images.githubusercontent.com/60228374/99711899-58d52700-2a70-11eb-9236-48c97e181717.gif)

### Tesselation of Voronoi Polygons

![Screen Shot 2020-11-19 at 12 14 06 PM](https://user-images.githubusercontent.com/60228374/99712456-152eed00-2a71-11eb-90b9-7a609f64d14f.png)

### Urbanized areas within Afar
![afar_v1](https://user-images.githubusercontent.com/60228374/99712887-a8682280-2a71-11eb-971b-cac830904d74.png)
