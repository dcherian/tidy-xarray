# Examples

This page contains examples of 'tidying' datasets. 

## 1. Aquarius

This is an example of tidying a dataset comprised of locally downloaded files. Aquarius is a sea surface salinity dataset produced by NASA and accessed as network Common Data Form (NetCDF) files.
You can find this example [here](https://gist.github.com/dcherian/66269bc2b36c2bc427897590d08472d7). This example focuses on data access steps and organizing data into a workable data cube. 

## 2. ASE Ice Velocity

Already integrated into the Xarray tutorial, this examples uses an ice velocity dataset derived from synthetic aperture radar imagery. You can find it [here](https://tutorial.xarray.dev/data_cleaning/ice_velocity.html). This example focuses on data access steps and organizing data into a workable data cube. 

## 3. Harmonized Landsat-Sentinel

This [example](https://nbviewer.org/gist/scottyhq/efd583d66999ce8f6e8bcefa81545b8d) features cloud-optimized data that does not need to be downloaded locally. Here, package such as [`odc-stac`](https://github.com/opendatacube/odc-stac) are used to accomplish much of the initial tidying (assembling an x,y,time cube). However, this example shows that there is frequently additional formatting required to make a dataset analysis ready.