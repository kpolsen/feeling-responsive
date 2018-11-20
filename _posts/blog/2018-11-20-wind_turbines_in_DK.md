---
layout: page
subheadline:  "Renewables"
title:  "Mapping all installed wind turbines in Denmark"
teaser: "A quick and dirty python script to map all offshore and onshore wind turbines in Denmark using the python basemap module."
header:
    image_fullwidth: "texture1.png"
image:
   thumb: "blog/2018-11-20/thumb.jpg"
categories:
    - blog
comments: true
---

<h2 style="color: #006699">Wind power in Denmark</h2>

In 2017, a world record 43.4% of all electricity consumption in Denmark was covered by wind power generated throughout the year. 
That makes Denmark an ideal place to study future scenarios of high penetatrion of renewables, which is at the focus of 
long term goals in many countries.  
For my research at the Technical University of Denmark, I study fluctuations in the residual power which is 
calculated as the difference between renewable power generation and consumption. 
This analysis can be done on different scales within Denmark, to study how fluctuations in residual power 
change as more and more wind turbines (and farms) are aggregated on the power supply side. 


<h2 style="color: #006699">So where are they?</h2>
On the website of ["Energistyrelsen"](https://ens.dk/service/statistik-data-noegletal-og-kort/data-oversigt-over-energisektoren#), 
one can find a list of all wind turbines currently installed in Denmark, 
with information attached such as their capacity and position. 
By reading that data into a pandas dataframe and using the [basemap python module](https://matplotlib.org/basemap/), 
we can get an overview of where all turbines are installed, here color-coded by regions relevant for 
my analysis (DK1, DK2 and Bornholm):

<img src="{{ site.urlimg }}/blog/2018-11-20/turbine_placement_mean_r.png" alt="" width="600">

The circles indicate the mean distance from all wind turbines to the capacity-weighted center position of all turbines in a specific region.

If you're interested, I uploaded the code on Github for public use:

<a class="radius button small" href="https://github.com/kpolsen/python-skills/tree/master/wind_turbine_placement">Go to the source code in jupyter notebook format›</a>

You can also get fancy, and make the following changes to load actual 2D imagery of the world:

```python
# m.fillcontinents(color='navajowhite',lake_color='lightcyan')
# m.drawmapboundary(fill_color='lightcyan')
m.arcgisimage(service =  "ESRI_Imagery_World_2D", xpixels = 2000, alpha=0.05)
```

Here, I also changed color of the DK1 turbine locations, in order so see them better:

<img src="{{ site.urlimg }}/blog/2018-11-20/turbine_placement_mean_r_epsg.png" alt="" width="600">

<!--
## How to embed a gallery

You just need to choose a template like the [`page`][3]- or [`page-fullwidth`][4]-template and then just use `{% raw %}{% include gallery %}{% endraw %}`.

`{% raw %}{% include gallery %}{% endraw %}` lets you easily embed a gallery into your post. To use the gallery-include...


### Step 1

1. Make two images: a thumbnail and a big image.
2. Name the thumbnail *gallery-image-thumb.jpg* and...
3. ...name the big *gallery-image.jpg*.
4. Place them in the *images*-folder.


### Step 2

Define the big version in frontmatter,  

~~~
gallery:
    - image_url: gallery-image.jpg
~~~

If you like captions, give each image a caption:

~~~
gallery:
    - image_url: gallery-image.jpg
       caption: Starting Page with huge One Logo
~~~

### Step 3

Add the include whereever you want in your content with `{% raw %}{% include gallery %}{% endraw %}`.

{% include alert info='Have a look at this example-entry. And have a look into the images-folder. :)' %}



## Other Post Formats
{: .t60 }
{% include list-posts tag='post format' %}



 [1]: http://foundation.zurb.com/docs/components/clearing.html
 [2]: http://foundation.zurb.com/docs/components/block_grid.html
 [3]: {{ site.url }}{{ site.baseurl }}/design/page/
 [4]: {{ site.url }}{{ site.baseurl }}/design/page-fullwidth/
-->
