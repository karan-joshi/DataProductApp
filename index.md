---
title       : Data Product App Pitch
subtitle    : 
author      : Karan Joshi
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## How Good Is Your Car Choice
This app is a fun app built to give you an idea of how good your choice of car is based on the car's metrics. The app utilizes a linear regression model built using R mtcars dataset to estimate the Miles Per Gallon based on Car's stats like number of cylinders, Horse Power, weight adn type of transmission.


--- .class #id 

## The Input Data Required For The App

- Number of Cylinders 
- Horse Power
- Weight
- Type of Transmission

--- .class #id 

## Reactive Result From The App

Based on the inputs, the model spits the Miles Per Gallon estimate. The app then uses that to make some interesting comments about the user's chouce of the car.

--- .class #id 

## Underlying Model


```r
#linear regression model
model <- lm(mpg ~ cyl + hp + wt + am, mtcars)

#sample data for demo
sampleData <- data.frame(cyl = 21, hp = 110, wt = 2, am = 0)

#result 
mpg <- predict(model, sampleData)

mpg
```

```
##        1 
## 12.54066
```
