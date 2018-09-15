

## This is my submission to STAT545 hw1.


## Brief Intro
Hello everyone. My name is Ke Rang. You can call me Yuki. I'm an MEng student in Electrical and Computer Engineering. 

I have encountered several requirements related to data visualization during my previous web development practices. Thus I wish to learn how to handle data in a "systematic" way. And that's why I'm here!

## Interests

![Yuki's interests](https://github.com/STAT545-UBC-students/hw01-yukirang/blob/master/interests.png)

### Expressions toward randomly picked heroes in Dota2
Hero | Emoji
------------ | -------------
Vengeful Spirit | :kissing_heart:
Viper | :blush:
Wraith King | :relieved:
Spirit Breaker | :flushed:
Earthshaker | :disappointed_relieved:
Meepo | :scream:

### Places I want to visit
* Singapore
* Hokkaido
* LA
* Bushan

### Favorite movie
Definitely the Resident Evil series!

![ ](http://www.sonypictures.com/movies/residentevilthefinalchapter/assets/images/onesheet.jpg)


## R exploration
I was inspired by the "Play Style" in Dota2 to show a radar graph of my interests, which is done by R, played with the "fmsb" library:

```R
# Library
library(fmsb)

# Create data: interests of Yuki Rang:
data=data.frame(
                Kpop=c(20),
                F1=c(7),
                travel=c(15),
                coding=c(17),
                Dota2=c(10),
                movie=c(11),
                photography=c(9))
colnames(data)=c("K-pop" , "F1" , "travel" , "coding","Dota2" , "movie", "photography")

# Add 2 lines to the dataframe: the max and min of each topic to show on the plot!
data=rbind(rep(20,10) , rep(0,10) , data)

# The default radar chart proposed by the library:
radarchart(data)

# Custom the radarChart !
radarchart( data  , axistype=1 , 
            
#custom polygon
pcol=rgb(0.9,0.5,0.5,0.9) , pfcol=rgb(0.8,0.5,0.5,0.5) , plwd=4 , 
            
#custom the grid and labels
cglcol="grey", axislabcol="black", caxislabels=seq(0,20,5), cglwd=0.8,vlcex=0.8)
```











