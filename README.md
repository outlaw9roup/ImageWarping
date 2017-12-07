# ImageWarping
Using IDW and RBF to achieve image warping.

## Ⅰ.Problem Description

The process of warping an image can devide into two steps:

1. Compute the desired displacement of all pixels in the source image.
2. Resample the image into create the output image.

This experiment focuses on the first step of image warping,construction of a suitable mapping function.

We will call this the "deformation" step. It is commonly performed either by applying a global analytic mapping function to 
the image pixel positions or by using a set of some control points that specify displacements of some point in the initial image.

We can formulate the problem of image deformation in terms of input and output:

Input: n pairs <a href="https://www.codecogs.com/eqnedit.php?latex=$&space;(\textbf{p}_i,\textbf{q}_i&space;)&space;$" target="_blank"><img src="https://latex.codecogs.com/gif.latex?$&space;(\textbf{p}_i,\textbf{q}_i&space;)&space;$" title="$ (\textbf{p}_i,\textbf{q}_i ) $" /></a> of control points
<a href="https://www.codecogs.com/eqnedit.php?latex=$&space;\textbf{p}_i,\textbf{q}_i&space;\epsilon&space;\textbf{IR}^{2},i=1,...,n&space;$" target="_blank"><img src="https://latex.codecogs.com/gif.latex?$&space;\textbf{p}_i,\textbf{q}_i&space;\epsilon&space;\textbf{IR}^{2},i=1,...,n&space;$" title="$ \textbf{p}_i,\textbf{q}_i \epsilon \textbf{IR}^{2},i=1,...,n $" /></a> .

output: An at-least-continuous function <a href="https://www.codecogs.com/eqnedit.php?latex=$&space;\textbf{f}:\textbf{IR}^{2}&space;\rightarrow&space;\textbf{IR}^{2}$" target="_blank"><img src="https://latex.codecogs.com/gif.latex?$&space;\textbf{f}:\textbf{IR}^{2}&space;\rightarrow&space;\textbf{IR}^{2}$" title="$ \textbf{f}:\textbf{IR}^{2} \rightarrow \textbf{IR}^{2}$" /></a> with <a href="https://www.codecogs.com/eqnedit.php?latex=$\textbf{f}(\textbf{p}_i)=\textbf{q}_i,&space;i=1,...,n.$" target="_blank"><img src="https://latex.codecogs.com/gif.latex?$\textbf{f}(\textbf{p}_i)=\textbf{q}_i,&space;i=1,...,n.$" title="$\textbf{f}(\textbf{p}_i)=\textbf{q}_i, i=1,...,n.$" /></a>

## Ⅱ.Algorithm Description

