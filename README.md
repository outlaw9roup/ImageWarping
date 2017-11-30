# ImageWarping
Using IDW and RBF to achieve image warping.

1.Problem Description

The process of warping an image can devide into two steps:

(1)Compute the desired displacement of all pixels in the source image.
(2)Resample the image into create the output image.

This experiment focuses on the first step of image warping,construction of a suitable mapping function.

We will call this the "deformation" step. It is commonly performed either by applying a global analytic mapping function to 
the image pixel positions or by using a set of some control points that specify displacements of some point in the initial image.

We can formulate the problem of image deformation in terms of input and output:

<script type="text/javascript" src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=default"></script>

$$x=\frac{-b\pm\sqrt{b^2-4ac}}{2a}$$
