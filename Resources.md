---
layout: page
title: Resources
---

Here is a very adhoc collection of websites and resources. This is not a comprehensive or organised list, it's mostly for me to be able to refer back to, but may be of use to some. 

#### Linear Model Related Things

  - For beginning: [Frans Rosenburg's incredible videos](https://fransrodenburg.github.io/Applied-Statistics/) plus associated teaching
  - For going deeper: [Tim Newbolds teaching](https://timnewbold.github.io/teaching.html) (esp on linear models - just so clear)
  - If understanding trends through time: Explorations in using 'year' as a random effect in linear models (conclusion: only useful if trying to get specific year estimates to e.g. correct for sampling bias. Not very useful if trying to simplify or generalise to estimate through time slopes). From [Andrew Heiss](https://www.andrewheiss.com/blog/2021/12/01/multilevel-models-panel-data-guide/#intercepts-and-slopes-for-each-country-account-for-year-specific-differences)


#### Causal Inference/Impact Evaluation Related Things

  - New to Causal Inference? Read [The Book of Why](https://blackwells.co.uk/bookshop/product/The-Book-of-Why-by-Judea-Pearl-Dana-Mackenzie/9780141982410?srsltid=AfmBOopcGL7t9hTuatMLimkq6HvVo3Dwprrpc8J9mkUp1Fg8cwpPhwh7)
  - [Brilliant, though technical, paper](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0231349) on why Two Way Fixed Effects are almost never the model you want (in particular if you are trying to generalise an estimate through time, or across groups - the TWFE model will give a point estimate for each group, in each time point, thereby not giving you any useful conclusions) 
    - [On why propensity scores are not good for matching](https://funginstitute.berkeley.edu/wp-content/uploads/2015/09/psnot.pdf) (also technical, but well worth committing to - there's a youtube video which the comments indicate explain it very clearly [here](https://www.youtube.com/watch?v=rBv39pK1iEs))


#### GIS Related Things

  - If you're totally new to spatial analysis: you can do most simple-medium advanced things in either R or a GIS interface software (e.g. ArcGIS or QGIS). Some very advanced spatial modelling requires ArcGIS, but you'll know if you need that. Different people find different approaches that work for them. Either way you need to understand spatial data types - running through [this resource](https://www.ecologi.st/spatial-r/index.html#general) is a good place to start - it also walks you through the basics of working in R. If you're a visual learning, you might find it better to download QGIS (which is free) and play about with data there a bit first to get a feel for it. [This video](https://www.youtube.com/watch?v=SovdBaus7pM) can kick you off.
  - BEWARE If you're doing spatial analysis in R, a few years back all the packages went through a total overhaul, making a lot of material out of date. If your googling leads you to use any of the following packages (raster, rgdal, rgeos, sp), IGNORE and look elsewhere. Ideally you should be conducting your spatial work in terra and/or sf.
  - [Intro to spatial analysis in R](https://rspatial.org/index.html) incl terra.

#### Miscellaneous!

  - Apparently nothing meeting this criteria in my brain just yet

#### Cool stuff I chat with my Nieblings about 
  - Just a giant snake https://www.nature.com/articles/nature07671 

