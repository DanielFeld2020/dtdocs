---
title: (deprecated) levels
id: levels
weight: 20
applicable-version: 4.4
tags: 
working-color-space: Lab
view: darkroom
masking: true
---

---

**Please note that this module is [deprecated](../../darkroom/processing-modules/deprecated.md) from darktable 4.4 and should no longer be used for new edits. Please use the [_rgb levels_](./rgb-levels.md) module instead.**

---

Adjust black, white and mid-gray points.

The levels tool offers two modes of operation:

manual
: The levels tool shows a histogram of the image, and displays three bars with handles. Drag the handles to modify the black, middle-gray and white points in absolute values of image lightness (the L value from Lab).

: Moving the black and white bars to match the left and right borders of the histogram will make the output image span the full available tonal range, increasing the image's contrast. 

: Moving the middle bar will modify the mid-tones. Move it to the left to make the image look brighter and move it to the right to make it darker. This is often referred to as changing the image's gamma.

: Three color pickers are available for sampling the black, white and gray points from the image. The "auto" button auto-adjusts the black and white point and puts the gray point exactly in the mean between them.

automatic
: The module automatically analyses the histogram of the image, detects the left and right histogram borders, and lets you define the black point, the gray point and the white point in terms of [percentiles](http://en.wikipedia.org/wiki/Percentile) relative to these borders.

---

**Note:** Under certain conditions, especially with highly saturated blue light sources, the _levels_ module may produce black pixel artifacts. See the "gamut clipping" option of the [_input color profile_](./input-color-profile.md) module for information about how to mitigate this issue.

---

# module controls

mode
: The mode of operation (automatic or manual).

black (automatic mode only)
: The black point in percentiles relative to the left border of the histogram.

gray
: The gray point in percentiles relative to the left and right borders of the histogram after having applied the black point and white point corrections.

white
: The white point in percentiles relative to the right border of the histogram.
