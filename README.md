# CV-Instagram-Filters
Python remake of the Gotham Instagram filter

## Four easy steps
Using numpy, scikit-image, and a profound artistic vision
(required to copy the most popular Instagram filter available)


# Original image
A nice shot, but with a dull colour palette. Really missing a lot of
potential detail around the sky and clouds - also colours look
desaturated, and white/black balance is off on both ends.
<p align="left">
  <img height=400 width=400 src="images/zell_am_see_snowboarding.jpg">
</p>


# 1. Mid tone colour boost
* Lets add some vibrancy.
<p align="left">
  <img height=400 width=400 src="images/2_mid_tone_colour_boost.jpg">
</p>
* Red snow and sky? I don't know about that..


# 2. Bluer Blacks
* Lets add some depth to the low end.
<p align="left">
  <img height=400 width=400 src="images/3_bluer_blacks.jpg">
</p>

# 4. Sharpening the image

This step take most of the time for executing the script.
It takes approximately 3s on an Odroid C2.

Now look at those fluffy trees,
<p align="left">
  <img height=400 width=400 src="images/4_sharpened.jpg">
</p>

# 5. Blue channel boost in lower-mids, decrease in upper-mids
<p align="left">
  <img height=400 width=400 src="images/5_blue_adjusted.jpg">
</p>

# 6. Finally, add a vignette for that vintage look
Final image on the left, original on the right.
<p align="left">
  <img height=400 width=400 src="images/6_add_vignette.jpg">
  <img height=400 width=400 src="images/zell_am_see_snowboarding.jpg">
</p>

### Summary

The depth of colours around the boots is nice, as is the extra contrast on the snow capped trees. The increased vibrancy has turned the snow and sky an unwanted redish colour - the vibrancy modification needs to be turned down on the R channel. Vignette looks good however I think i'd like to see it even stronger.
<p></p>

Overall, it's turned a dull shot into a great playful image. All while maintaing true to the original Instagram Gothom filter.

### Execution Time on Odroid C2
1. With image saving at each step :  
```
# python -W ignore gotham.py
  Instagram Filter Remake: Gotham
  Elapsed time: 6.295s
```
2. Without image saving :
```
# python gotham.py 
  Instagram Filter Remake: Gotham
  Elapsed time: 4.848s
```

### Installation on Odroid
1. Install SciPy following [this guide](https://www.scipy.org/install.html). basically running this :  
`sudo apt-get install python-numpy python-scipy python-matplotlib ipython python-pandas python-sympy python-nose`

2. Install Cython (required to build scikit-image)  
`apt install cython`

3. Install `scikit-image` (new version of `skimage`)  
`pip install scikit-image`


