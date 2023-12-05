# tidy-xarray

Authors: Emma Marshall, Deepak Cherian, Scott Henderson  

This project aims to define a `tidy` framework for array datasets represented by Xarray data structures. Currently, we focus on geospatial use cases and remote sensing datasets. We welcome community contributions, and would be particularly excited to connect with users of model output datasets interested in tidy principles. 

Much of this work was the subject of a presentation at the 2023 SciPy Conference. The slides can be found in the [Proceedings of the 22nd Python in Science Conference](https://conference.scipy.org/proceedings/scipy2023/slides.html).

## What is tidy data?

[Tidy data](https://vita.had.co.nz/papers/tidy-data.pdf) is a concept defined by Hadley Wickham for tabular datasets in the R programming language. Tidy data focuses on the workflow steps of preparing a dataset for analysis and doing so in a way that simplifies rather than complicates further analysis. Wickham defines 'tidying' as "structuring datasets to facilitate analysis" such that the structure of a dataset reflects its semantics (Wickham, 2014). 

### Tidy data resources 

1. [R for Data Science chapter on Tidy data](https://r4ds.hadley.nz/data-tidy.html)
2. [Tidy data, Journal of Statistical Software](https://vita.had.co.nz/papers/tidy-data.pdf)

## What are datacubes?

There are very helpful resources that conceptualize datacube representations of data. We highly recommend [this](https://openeo.org/documentation/1.0/datacubes.html#what-are-datacubes) page by openEO on datacubes for a comprehensive explanation of datacube characteristics and general computation patterns. 

## What do we hope to do? 

As listed above, many great resources define and explain working with geospatial array data. Our goal isn't to recreate the wheel but to define specific guidelines for formatting Xarray data structures in ways that will simplify analytical workflows. You can find a condensed version of this material in the [Xarray Tutorial section on data tidying](comingsoon). In this repository, you will find descriptions and explanations of `tidy` principles for Xarray data objects as well as examples of 'untidy' datasets and step-by-step explanations of the process of 'tidying' them. 

## Contributing

We would love your help and engagement on this project! If you have a dataset that you've worked with that felt particularly messy, or one with steps you find yourself thinking back to as you work with new datasets, consider submitting it as an example! If you have input on tidy principles, please feel free to raise an issue. 
