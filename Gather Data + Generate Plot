#Run Production Analysis In Major League Baseball 

#Load Packages
library(Lahman)
library(dplyr)
library(ggplot2)

#Cull Data & Identify Relevant Variables
totalRS <- Teams %>% select(yearID, R, G) %>% mutate(AvgRperG = R/G) %>% group_by(yearID) %>% summarise(sum(AvgRperG))
names(totalRS) <- c("yearID", "RUN")
head(totalRS)
View(totalRS)

#Generate Plot
ggplot(data = totalRS, aes(x = yearID, y = RUN)) + stat_smooth() + geom_line()
