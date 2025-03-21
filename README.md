# Gopher-Rockfish-Lengths-in-MPAs-and-Reference-Sites

## Introduction

Marine protected areas (MPAs) are areas of marine space preserved and protected from human influence which are integral to the health and continuation of many marine species. In order to determine the MPA effect on fish popuations hook and line surveys are conducted to compare the lengths of fish species from the MPAs to non-protected areas with similar ecological characteristics called reference sites. The size of a fish is directly related to fecundity and survivability, therefore if MPAs are working as intenteded, fish caught in MPAs should on average be larger than those caught in reference sites. The aim of this project is to use the gopher rockfish, a common nearshore fish species, as a model species to determine if the MPAs Point Lobos and Año Nuevo in central California are having a signficant impact on the fish populations. 

## Methods

The dataset is comprised of length (cm) of the gopher rockfish, area (0=Point Lobos, 1=Año Nuevo), site (0=referene site, 1=MPA) and year. This was subset into four datasets in which there was the Point Lobos MPA and referene datasets and the same for Año Nuevo. A linear regression model was created for each dataset in the form of length ~ 1 + year. 10,000 simulations we run on each linear regression model and the Beta1 estimated coefficient was pulled and averaged to determine the slope of the relationship which is insight to the strength of the MPA effect. Posterior predicitive modeling was then used to estimate the average gopher rockfish length for 2025 in the respective MPA location. 

## Figures 
![Año Nuevo Gopher Rockfish Length](https://github.com/user-attachments/assets/d831d410-3456-491e-b308-71d19deb5c34)

![Point Lobos Gopher Rockfish Length](https://github.com/user-attachments/assets/7057f92c-9363-464e-a48c-bbccd2d85d06)

## Conclusion 

From the linear regression models I found that Año Nuevo average length of gopher rockfish increases by 0.1588 cm/yr (95% CI: 0.1353, 0.1827) as opposed to its refernce site which showed nearly no change in average length at -0.0014 cm/yr (95% CI: -0.0419, 0.0388). The probability that the average length increases in the Año Nuevo MPA was greater than its reference site is 100%. Looking at Point Lobos MPA the average length of gopher rockfish increases by 0.1435 cm/yr (95% CI: 0.1238, 0.1631) compared to its refernece site slowly increasing by 0.0715 cm/yr (95% CI: 0.0318, 0.1127). The probability that the average length increases in the Point Lobos MPA was greater than its reference site is 99.89%. Given these two examples the MPA effect is real and is resulting in larger fish growth in the same amount of years on average than compared to non-protected areas. 

Lastly, I compared the average MPA effect of Point Lobos to Año Nuevo to determine which had the stronger effect as it is theorized that the MPA effect is directly correlated to the area. Año Nuevo MPA covers 11.5 square miles and Point Lobos MPA covers 14.21 square miles, so I expected to see Point Lobos with a more significant slope. However, the confidence intervals of the two slopes overlap so they are not significantly different from one another, so the theory may not apply and MPA effect based on other environmental factors or the size difference was not large enough to show significant results. I also used posterior predictive modeling to determine the average length for gopher rockfish in 2025 in the MPAs based on the linear regression models. For Point Lobos it was 29.21 cm and for Año Nuevo it was 30.73, which again shows that there was not much difference in the MPA effect as the size difference is neglible. 

## Dependencies

Only install into Rstudio and ensure that all packages are installed properly. 

Data was obtained from the CCFRP open data and cleaned to included only information on gopher rockfish and their length, site and area. The link to access the raw data is included below. 

https://data.ca.gov/dataset/california-collaborative-fisheries-research-program

## Author

Konnor Payne

konnormpayne@gmail.com
