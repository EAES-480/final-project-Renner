---
title: "README"
author: "Amelia Renner"
output: html_document
---

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
```

# Introduction

FIA data are collected on permanent plots around the US; this set is from Alaska. Each case is a tree measured in a plot in a year. The same trees are measured year after year. The variables relate to tree carbon storage; the ones I am most interested in are my outcome variable (total tree carbon) and a few of explanatory variables (downed woody debris, elevation, longitude/latitude, and forest type).

These data are unique because they are so spatially uniform; there is one plot for roughly every 6500 square acres. Thus, it is possible to investigate the relationship between total tree carbon and latitude.

### Question

How does variability in total forest carbon change along a latitudinal gradient in Alaska?

### Variables

| Variable | Description |
|------------------------------------|------------------------------------|
| Carbon Ratio (`carbonratio`) | Daily burnt area in hectares |
| Standing Dead Carbon (`standingdead_C_gm2`) | Carbon stored in dead trees (grams carbon / square meter) |
| Living Tree Carbon Storage (`livetree_C_gm2`) | Carbon stored in live trees (grams carbon / square meter) |
| Below Ground Biomass (`BGtree_C_gm2`) | Carbon stored below ground in living trees (grams carbon / square meter) |
| Total Tree Carbon (`total_treeC_gm2`) | Live carbon mass (grams carbon / square meter) |
| Net Primary Productivity (`NPP_C_gm2y`) | Net rate of productivity (biomass production) after accounting for respiration (grams carbon / square meter) |
| Dead Wood Carbon Stock (`biomass.dead.C.gm2`) | Carbon stored in dead wood (fallen trees, woody debris) (grams carbon / square meter) |
| Live Tree Biomass (`biomass.live.C.gm2`) | Biomass of living trees, aboveground (grams carbon / square meter) |

# Methods

*Outcome variable* - variability (standard deviation) in total tree carbon (grams carbon / square meter)

*Predictor variables* - latitude

Using a robust bootstrapping method, I will use a 1000 resample with replacement method to estimate how much variation is in the true population of trees in southeastern Alaska.

# Results & Conclusion

There is a large amount of variability in the 59-60 degree latitude band; it is nearly 10 times as variable as the next most variable band. There is less variability in the most poleward latitude bands of this region. This means that the most representative samples are the most poleward bands, and the innermost latitude bands are more sensitive to individual samples and are less representative of the population as a whole.
