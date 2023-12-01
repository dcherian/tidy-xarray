# Introduction

Array data that are represented by Xarray objects are often multivariate, multi-dimensional, and very complex. Part of the beauty of Xarray is that it is adaptable and scalable to represent a large number of data structures. However, this can also introduce difficulty (especially for learning users) in arriving at a workable structure that will best suit one's analytical needs. 

This project is motivated by community sentiment and experiences that oftentimes, the hardest part of learning and teaching Xarray is teaching users how best to use Xarray conceptually. We hope to leverage the experiences of Xarray and geospatial data users to arrive at a unifying definition of 'tidy' data in this context and best-practices for 'tidying' geospatial raster data represented by Xarray objects. 

## A brief primer on tidy data

Tidy data was developed by Hadley Wickham for tabular datasets in the R programming language. There are great resources that comprehensively explain this concept and the ecosystem of tools built upon it. Below is a very brief explanation:

**Data tidying** is the process of structuring datasets to facilitate analysis. Wickham writes: "...tidy datasets are all alike but every messy dataset is messy in its own way. Tidy datasets provide a standardized way to link the structure of a dataset (its physical layout) with its semantics (its meaning)" (Wickham, 2014). 

### Tidy data principles for tabular datasets
The concept of [tidy data](https://vita.had.co.nz/papers/tidy-data.pdf) was developed by Hadley Wickham in the R programming language, and is a set of principles to guide facilitating tabular data for analysis. 

```
"Tidy datasets are all alike but every messy dataset is messy in its own way." - Wickham, 2014
```

Wickham defines three core principles of tidy data for tabular principles. They are:

1. Each variable forms an observation
2. Each observation forms a row
3. Each type of observational unit forms a table

## Imagining a 'tidy data' framework for gridded datasets

### Common use-case: Manipulating individual observations to an x-y-time datacube

Data downloaded or accessed from DAACs and other providers is often (for good reason) separated into temporal observations or spatial subsets. This minimizes the services that must be provided for different datasets and allows the user to access just the material that they need. However, most workflows will involve some sort of spatial and/or temporal investigation of an observable, which will usually require the analyst to arrange individual files into spatial mosaics and/or temporal cubes. In addition to being a source of duplicated effort and work, these steps also introduce decision-points that can be stumbling blocks for newer users. We hope a tidy framework for xarray will streamline the process of preparing data for analysis by providing specific expectations of what 'tidied' datasets look like as well as common patterns and tools to use to arrive at a tidy state. 

## Tidy data principles for Xarray data structures

These are guidelines to keep in mind while you are organizing your data. To see the examples that were used to develop these principles, go [here]. 

**1. Dimensions** 
- Minimize the number of dimensional coordinates

**2. Coordinates**
- Non-dimensional coordinates can be numerous. Each should exist along one or multiple dimensions

**3. Data Variables**
- Data variables should be observables rather than contextual. Each should exist along one or multiple dimensions.

**4. Contextual information (metadata)**
- Metadata should only be stored as an attribute if it is static along the dimensions to which it is applied.
- If metadata is dynamic, it should be stored as a coordinate variable.

**5. Variable, attribute naming**
- **Wherever possible, use cf-conventions for naming**
- Variable names should be descriptive
- VAriable names should not contain information that belongs in a dimension or coordinate (ie. information stored in a variable name should be reduced to only the observable the variable describes.

**6. Make us of & work within the framework of other tools**
- Tools like STAC, open data cube, cf.xarray, pystac, stackstac (and more) make tidying possible and smoother, especially with large, cloud-optimized datasets.

## Other guidelines and rules of thumb

- Avoid storing important data in filenames
- Non-descriptive variable names can create + perpetuate confusion
- Missing coordinate information makes datasets harder to use
- Elements of a dataset's 'shape'/structure can sometimes be embedded in variable names; this will complicate subsequent analysis

## Contributing

This project is an evolving community effort. **we want to hear from you!**. If reading this description and examples reminded you of your own experiences tidying datasets to prepare them for analysis, please consider submitting an example to our [data tidying gallery](insert page here). Your experience could help other users! 
