---
author: Jinji
date: "2021-07-28"
title: R Language Notes
slug: "en/r"
---

# C

## Color

- add more colors to a color palette

```r
library(RColorBrewer)
# Define the number of colors you want
nb.cols <- 18
mycolors <- colorRampPalette(brewer.pal(8, "Set2"))(nb.cols)
# Create a ggplot with 18 colors 
# Use scale_fill_manual
ggplot(df) + 
  geom_col(aes(name, Sepal.Length, fill = factor(Sepal.Length))) +
  scale_fill_manual(values = mycolors) +
  theme_minimal() +
  theme(legend.position = "top")
```


# L

## Legend

- change legend size

```r
ggplot(data, aes(x=x, y=y)) +
  theme(legend.key.size = unit(1, 'cm'), #change legend key size
        legend.key.height = unit(1, 'cm'), #change legend key height
        legend.key.width = unit(1, 'cm'), #change legend key width
        legend.title = element_text(size=14), #change legend title font size
        legend.text = element_text(size=10)) #change legend text font size
```







