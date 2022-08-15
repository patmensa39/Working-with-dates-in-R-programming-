# Working with dates and times in R programming 
library(tidyverse)
library(lubridate)


weather<- read_csv("http://594442.youcanlearnit.net/mexicanweather.csv")
weather

weather <- weather %>% 
  mutate(year = year(date), month = month(date), day = day(date))

weather

#Checking the day of the week months and year 
mday('1955-04-01')
wday('1955-04-01')
yday('1955-04-01')

### Building your own dates 
### American standard 
mdy('04/01/2020')

#European standard '
dmy('04/01/2020')

