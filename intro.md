# Tidy geospatial cubes

This Jupyter Book accompanies the 2023 SciPy presentation `Tidy Geospatial Cubes`. Here you will find jupyter notebook examples of the dataset tidying steps and concepts we discuss in the presentation. 

## What is tidy data? 

The concept of [tidy data](https://vita.had.co.nz/papers/tidy-data.pdf) was developed by Hadley Wickham in the R programming language, and is a set of principles to guide facilitating tabular data for analysis. 

```
"Tidy datasets are all alike but every messy dataset is messy in its own way." - Wickham, 2014
```
## How could a tidy framework help users of geospatial array data?

Geospatial datasets can be large, complex and cumbersome to work with, especially with users who are new to python/xarray. Conversations at conferences, Pangeo community meetings and elsewhere highlight the common experience that hardest part of learning (and teaching) xarray is conceptualizing xarray data structures and understanding how to coerce one's data into them. Specifically, this comes down to:
  - What are coordinates, dimensions, variables, and attributes? How do they all inter-relate?
  - How to structure your data within the xarray framework
  - How to store metadata 

In particular, we see a lot of duplicated effort, and hence, potential utility in a 'tidy' framework or tidy guidelines, in the initial data processing steps of assembling downloaded data (usually divided on disc into temporal observations, or spatial subsets) into logical cubes with an (x,y,time) structure. Gridded n-dimensional datasets as they are accessed from data providers are often separated into temporal observations and spatial subsets. Most workflows will involve some sort of merging and concatenation of these objects. At minimum,


Where we see a specific utility for a tidy framework is in steps to prepare gridded datasets for analysis. Datasets downloaded or accessed from DAACs and other providers are often (for good reason) separated into temporal observations or spatial subsets. This minimizes the services that must be provided for different datasets and allows users to access just the material that they need. But we know that most workflows will involve spatial and/or temporal investigation of an observable, which will usually require the analyst to arrange individual files into spatial mosaics and/or temporal cubes. 

If most workflows contain the aforementioned steps, at minimum, this represents a large degree of duplicated effort across users. It also introduces many decision-points that can be stumbling blocks for newer users. We hope that a tidy framework for array data in xarray could streamline this process by providing a specific expectation of what a 'tidy' or 'analysis-ready' dataset looks like as well as common patterns and tools that one can use to arrive at this structure. 

## Examples of tidying data

### 1. [Aquarius](https://gist.github.com/dcherian/66269bc2b36c2bc427897590d08472d7)
### 2. [ASE Ice Velocity](https://tutorial.xarray.dev/data_cleaning/ice_velocity.html)
### 3. [Harmonized Landsat sentinel](https://nbviewer.org/gist/scottyhq/efd583d66999ce8f6e8bcefa81545b8d)

## Notes

We hope this is just the beginning of a conversation on what `tidy` xarray datasets could look like. Please reach out to us (via email or github), and share your experiences, thoughts, and opinions about these ideas! We recognize that these 'data tidying steps' (preparing data for analysis) are things that many of us have been doing for years and developing our own strategies for. We see this as an exciting opportunity to leverage individual knowledge and experiences toward a community structure that hopefully helps user experiences in the future. 

SciPy 2023 presentation slides [here](https://docs.google.com/presentation/d/e/2PACX-1vROHgszqaKr-TM5cRKUCDnprRw9Uc2vakZJVuE7-QhjFf4_GiNuMaLPH4yj_-lQdt6u40KGNuUiNxyI/pub?start=false&loop=false&delayms=3000#slide=id.g2314f44127a_0_532).

