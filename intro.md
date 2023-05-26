# Tidy xarray geospatial cubes

```{note}
just adding some filler text to this/other pages for now
```
This Jupyter Book accompanies the 2023 SciPy presentation `Tidy Geospatial Cubes`. Here you will find introductory material, information on how to access the example datasets used in the presentation and jupyter notebook examples of the dataset tidying steps and concepts we discuss in the presentation. 

brainstorming notes and draft google slides can be found [here](https://docs.google.com/presentation/d/1mDS_NWNyJBXVnehe5fQYZdHw4fQ1_j9DkqTLfPbpjvs/edit?usp=sharing)

## What is tidy data? 

The concept of [tidy data](https://vita.had.co.nz/papers/tidy-data.pdf) was developed by Hadley Wickham for the R programming language, and is a set of principles to guide facilitating tabular data for analysis. 

## Why do we need it for gridded geospatial data?

- copy here from slideshow and expand:
### Geospatial datasets are large, complex and can be cumbersome to work with, especially for people learning python / xarray. 
- Community sentiment (AGU convos, Tim Crone Pangeo showcase 2/15) that the hardest part of learning to use xarray is conceptualizing xarray structures and how to coerce your data into them 
  - What are coordinates, dimensions, variables? How do they all inter-relate?
  - How to structure your data within the xarray framework
  - How to store metadata 
  - Others? 
  - Some info about dataset size, complexity, maybe a schematic


## Examples of tidying data

### 1. [Harmonized Landsat sentinel](tidy_hls.ipynb)

### 2. [Aquarius](tidy-xarray.ipynb)

### 3. [ITS_LIVE](tidy_itslive.ipynb)

## Common 'tidying' steps for geospatial raster data

1. data is normally stored such that individual observations or time-steps are organized as individual files. To construct a usable 'data cube' one will need to read and organize many files
2. individual file names will often contain important metadata that needs to be used for indexing and selection later -- how to store it?

### How to know if something should be a dimension, coordinate or data variable? 

Complicated, but when in doubt, good rule is:  


    1. dimensional coordinates (ie. `dims`) should be `(x,y,time)`  
    2. non-dimensional coordinates (`coords`) should be anything that provides information about the independent data you are hoping to observe, but might not be fundamental to the shape/structure of your 'data cube'. Examples could be: imaging mode, polarization, temporal baseline. Often times, this information will be stored in the original filename, or potentially as an attribute. If it is something you might want to use for indexing or selection down the line, it is best to store that information as a non-dimensional coord.   
    3. Independent data variables (observables such as temperature, salinity, magnitude of velocity, reflectance, backscatter ...) should be stored as `data_vars`.

## What are the core concepts of tidy geospatial data cubes? 


## Caveats and issues

- what if there is 'contextual' info or metadata that you'd like to be able to index and select on, but there are duplicate values? eg. elevation, or coverage % -- best to keep those as vars?     