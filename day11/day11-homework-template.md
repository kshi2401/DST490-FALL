# Day 11 - Homework Responses
Khalid Shire

## Preliminaries

    Reading layer `Zip_Codes' from data source 
      `/Users/khaildshire/Downloads/DST 490/DST490 FALL/day11/shapefiles/Zip_Codes' 
      using driver `ESRI Shapefile'
    Simple feature collection with 75 features and 5 fields
    Geometry type: MULTIPOLYGON
    Dimension:     XY
    Bounding box:  xmin: 439356.4 ymin: 4959128 xmax: 486031.7 ymax: 5010414
    Projected CRS: NAD83 / UTM zone 15N

Link to google doc for instructions:
[LINK](https://docs.google.com/document/d/1shtTHzs8y09XZd86nKNFVSGjtsa-s8XVoalSJ5kyDpk/edit?usp=sharing)

<div style="background-color: #f0f8ff; border-left: 5px solid #007acc; padding: 10px;">

## (20 points) Code of Ethics

I’m interested in understanding your process for completing all the
questions in this assignment. Please tell me about the tools and
resources—including any use of AI—that helped you with your work. Please
remember to follow the outlined [Code of
Ethics](https://docs.google.com/document/d/1lMvzPTGUAaMnH0KPibShQ1ualuo8uqICCexkh8zmsW8/edit?usp=sharing).
Because our understanding of how to work with AI tools is emerging,
please err on the side of including too much detail rather than too
little.

I mostly used AI to help me troubleshoot R to read in the zipcode
shapefile, and to polish my grammar.

</div>

## Problem 1 (10 points)

Review [Chapter 18 in Modern Data Science with
R](https://mdsr-book.github.io/mdsr2e/ch-spatial2.html). Now that we
have had a few days on shapefiles and maps, what interesting things did
you learn about working with shapefiles?

Something I learned about working with shapefiles is that they’re just
data tables with a special geometry column that holds the shapes. The
most interesting part was that the map and the data need a shared ID to
connect. In my previous homework, the case data only had zip codes, but
the census tract map only had tract IDs, and the municipality map only
had city names. None of them matched my data, so I had to find a zip
code map that did.

## Problem 2 (10 points)

Read Chapters 1 and 2 and skim a few other chapters of interest from
[Analyzing US Census Data: Methods Maps, and Models in
R](https://walker-data.com/census-r/index.html). What did you learn
about the US Census Data and how could you use that to level up your
data science skills?

Something I learned is that the tidycensus package lets you pull Census
data straight into R in a clean format, so you don’t have to download
files from different websites. A way I could level up my data science
skills is by using the Census data to add context to my project, like
income or population by area, and then try mapping it.

## Problem 3 (20 points)

In our work in class, when we glimpsed the data frame `hennepin_zips`,
more data than just population was included. Select another variable and
make an aggregate chlorpleth map of the zip code areas for Hennepin
County. Use either `ggplot`, `mapview`, or `tmap`.

    Warning: package 'zipcodeR' was built under R version 4.5.2

![](day11-homework-template_files/figure-commonmark/unnamed-chunk-2-1.png)

## Problem 4 (20 points)

(10 points) The R package
[tidycensus](https://walker-data.com/tidycensus/index.html) has
information at the census tract level from the American Community Survey
or the Decennial census. Read through the basic usage of this package:
[LINK](https://walker-data.com/tidycensus/articles/basic-usage.html).

Discuss with your Hennepin County group the types of variables collected
from the American Community Survey. What variables might be of use in
your project. (One person can submit on behalf of your group. Since you
are submitting individual homework, if you aren’t the person submitting,
please tell me who is submitting in your response.)

I encourage you to start working with this package - notice that you
need an API key, but it is easy to obtain.

Sabine answered this question for the group on her homework :)
