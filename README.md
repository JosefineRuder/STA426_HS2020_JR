---
title: "STA426_Exercise_1a"
output: html_document
---

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
library(readxl)
library(ggplot2)
```

***

## Welcome to my first repository

Check out the recent data on the **covid19 pandemic** in switzerland here:

[Swiss Corona Data](https://www.corona-data.ch/>)

This is the reason why we have to take this course remotely. The question we all have in mind....


## Are we there yet?

![](C:\Users\fine_\Documents\Kurse\STA426_HS2020/picture_coronapandemia.png)

***


## Graph on the current daily cases in switzerland:

```{r graph corona}

corona_data <- read_excel("~/Kurse/STA426_HS2020/200325_Datengrundlage_Grafiken_COVID-19-Bericht.xlsx",  range = "A7:B208", col_names = TRUE)

ggplot(corona_data, aes(x= Datum, y= `Fallzahlen pro Tag`))+
  geom_point() +
  geom_smooth(span =0.1)
```

So the answer is *nope*, we are not there yet, second wave welcome.

***

##Advantages and Disadvantages of this Crisis


Negative aspects | Positive aspects
---| ---
No festivals and concerts | No crowded rooms with bad air
No travelling | Less pollution
No hugging of people I like | No hugging of people I don't like

***
