
### Origin-Destination (OD) Matrix 

odm <- pivot_wider(data = flows, id_cols = NODEI, names_from = NODEJ, values_from = PrdMIG)

odm <- odm[ ,-1]

odm <- odm[ ,c(16,2:15)]

![Screen Shot 2020-11-19 at 1 59 22 PM](https://user-images.githubusercontent.com/60228374/99711229-88cffa80-2a6f-11eb-8871-fc9f86775c19.png)

This is a snippet to reveal what my OD matrix looked like. 
