# assignment 6
A review of the moveHMM package

## Location
the package `moveHMM` can be found on [CRAN](https://cran.r-project.org/web/packages/moveHMM/index.html) and [GitHub](https://github.com/TheoMichelot/moveHMM).

## Vignette
the `moveHMM` package contains 3 vignettes.
1. The [guide to using moveHMM](https://cran.r-project.org/web/packages/moveHMM/vignettes/moveHMM-guide.pdf) provides a general description for the functionality of the package and provides the basic outline for the steps needed to use the functions in an analysis.
2. A [workflow example](https://cran.r-project.org/web/packages/moveHMM/vignettes/moveHMM-example.pdf) that shows all of the steps to use `moveHMM` in an analysis including the data cleaning process and the data visualization.
3. The last vignette is on the specific topic of [initial parameters](https://cran.r-project.org/web/packages/moveHMM/vignettes/moveHMM-starting-values.pdf) which provides descriptions for the parameters in this model. It also discusses best practices for setting initial values.

## Applications
An [article]( https://doi.org/10.1111/2041-210X.12578) was published in *Methods in Ecology and Evolution* discussing the model type and the `moveHMM` package.

## Review
This package is solely focused on the analysis of movement data using the Hidden Markov Model. It requires users to pre-format data as well as graphically represent results using other packages (e.g. tidyverse). This makes the use very simple for the user as the entire workflow of the package itself is based around the `fitHMM` function. All functions either prepare data for input into `fitHMM` or provide information about the model being fit. The only problem I have had with the package so far is that it seems like the model is fairly slow to fit. It takes me about 6 minutes for me to fit 50,000 GPS points. This is not a problem specifically for me since 5 minutes is still not that much. However, if you had a much larger data set you would be waiting a lot longer and may have to take deliberate steps to test how the model works before running the entire data set.
The vignettes provide enough information to get anyone with data started using the package, even if they do not have a strong understanding of the underlying statistics. They walk through all of the steps that you are likely to encounter to produce a well-fitting model. One thing lacking from the vignettes is an explanation for the resulting output of the model. Some explanation for the various output variables and their interpretation would be beneficial to users new to this model type. Although, this seems to be standard practice for analytical modeling packages in R. 
