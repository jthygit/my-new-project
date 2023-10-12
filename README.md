<!-- This is the markdown template for the final project of the Building AI course, 
created by Reaktor Innovations and University of Helsinki. 
Copy the template, paste it to your GitHub README and edit! -->

# Using AI in interpretation of satellite data

Final project for the Building AI course

## Summary

Remote sensing data has been available since invention of photography and manned flight. Observing the changes in Earth are becoming more and more important e.g. in undertanding climate change and its effects. Knowing how a geographic location has changed over time is very useful in cases like deforestation, desertification, change in build areas or military installations etc. The application areas are endless and the amount of data is HUGE. AI is used more and more also in this area. For example satellite imagery is being interpreted by artificial intelligence. IBM and NASA have created an open-source AI model for analyzing satellite data. This model is available on Hugging Face platform and was released in August 2023 (Source: https://newsroom.ibm.com/2023-08-03-IBM-and-NASA-Open-Source-Largest-Geospatial-AI-Foundation-Model-on-Hugging-Face). This project aims to give a short introduction to this topic.

## Background

Application arae for analyzing and interpretation of remote sensing data is vast. Here we concentrate on the burn scar detection, which is available at Hugging Face as a demo. In the demo on Hugging Face platform the user can use Prithvi model with own data. Prithvi is a temporal Vision transformer pretrained by the IBM and NASA team on continental US Harmonised Landsat Sentinel 2 (HLS) data for detecting burn scars. A lot of fires rage arcoss different continents e.g. in Canada large areas burn every year - see for example: https://cwfis.cfs.nrcan.gc.ca/interactive-map OR NASA's FIRMS (Fire Information for Resource Management System). Personal interest comes from GIS (Geographic Information Systems) and my involment in this field. Due to this data from Earth is near to my heart. During recent years we've seen increase in fires due to the extreme droughts around the globe e.g. in Southwestern United States. Knowing which areas are affected is important for example for science. The Prithvi model ins diverse and can be trained to detect different things. Among these are are crop classification and floods from which there are also demos. 

## How is it used?

Describe the process of using the solution. In what kind situations is the solution needed (environment, time, etc.)? Who are the users, what kinds of needs should be taken into account?

The end users (govermental officials, researchers or other interested parties) need to provide an HLS geotiff image, including the following channels in reflectance units (e.g. 0-1): Blue, Green, Red, Narrow NIR, SWIR, SWIR 2. The input for the model is a color composite image in geotiff from channels mentioned previously. Demo includes three test images to demostrate the model. Gathering and preprocessing suitable ("own") demo data is beyond the scope of this introduction.        

Below you can see an example of part of the possible input data for the model. A Sentinel-2 SWIR (Shortwave infrared) image with bands B12 (2190 nm), B8A (865 nm) and B4 (665 nm) that would be part of the input color composite (SWIR, Narrow NIR, Red) image. 
![Cat](2023-10-06-00_00_2023-10-06-23_59_Sentinel-2_L2A_SWIR.jpg)

## Data sources and AI methods
User can get satellite data (in this case HLS) from various sources. Here are two examples: NASA's Earthdata (https://www.earthdata.nasa.gov/) and EU's Copernicus Data Space Ecosystem (https://dataspace.copernicus.eu/). Two useful tools under these sevices are the "Worldview" and "Browser". A word of warning... when the size of the geographical area grows. So does the data file size. More technical details about the data can be found behind this link: https://huggingface.co/ibm-nasa-geospatial/Prithvi-100M-burn-scar. More details about the HLS data can be found here: [HLS data](https://www.earthdata.nasa.gov/esds/harmonized-landsat-sentinel-2#:~:text=The%20Harmonized%20Landsat%20Sentinel-2%20%28HLS%29%20project%20is%20an,product%20with%20observations%20every%20two%20to%20three%20days).

[Twitter API](https://developer.twitter.com/en/docs)

## Challenges

What does your project _not_ solve? Which limitations and ethical considerations should be taken into account when deploying a solution like this?

## What next?

How could your project grow and become something even more? What kind of skills, what kind of assistance would you  need to move on? 


## Acknowledgments

* list here the sources of inspiration 
* do not use code, images, data etc. from others without permission
* when you have permission to use other people's materials, always mention the original creator and the open source / Creative Commons licence they've used
  <br>For example: [Sleeping Cat on Her Back by Umberto Salvagnin](https://commons.wikimedia.org/wiki/File:Sleeping_cat_on_her_back.jpg#filelinks) / [CC BY 2.0](https://creativecommons.org/licenses/by/2.0)
* etc
