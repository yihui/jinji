---
author: Jinji
date: "2021-07-28"
title: R Language Notes
slug: "en/r"
---

## Disclaimer 
> To save my time finding codes(since I can't remember all of them), I made some notes here. These codes were all from online resources and I might have made some adjustments or might not. Copyright belongs to the original author, please inform site owner if any infringement. 


# C

## Color

- add more colors to a color palette

```r
library(RColorBrewer)
# Define the number of colors you want
nb.cols <- 13
mycolors <- colorRampPalette(brewer.pal(12, "Set3"))(nb.cols)
# Set3 has 12 colors
# Create a ggplot with 13 colors 
# Use scale_fill_manual
plot<-ggplot(df, aes(x = x var, y = y var, fill = some factor)) + 
  geom_bar(stat = "identity")+ylab("YY")+
  theme(axis.text.x = element_text(angle = 90))+
  theme(axis.title.x = element_blank())+
  scale_fill_manual(values =mycolors)

```


# L

## Legend

- change legend size

```r
ggplot(df, aes(x=x var, y=y var)) +
  theme(legend.key.size = unit(1, 'cm'), #change legend key size
        legend.key.height = unit(1, 'cm'), #change legend key height
        legend.key.width = unit(1, 'cm'), #change legend key width
        legend.title = element_text(size=14), #change legend title font size
        legend.text = element_text(size=10)) #change legend text font size
```







