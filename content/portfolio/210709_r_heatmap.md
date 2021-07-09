+++
date = "210709"
title = "R: heatmap"
draft = false
image = "img/portfolio/heatmap_458x500.png"
showonlyimage = false
weight = -210709
+++

2021-07-09

<!--more-->

The representation of associations between two classes of features becomes
complex when the number in each class increases and this occurs for instance
when investigating:

- genes to clinical parameters.
- mRNA to miRNA.
- subjects to lifestyles.

Heatmap is a regular proposition, but can be confusing, and it should be
carefully designed so as to help identifying the most relevant associations
between individual features or group of features. In the example below:

- The association between a row feature and a column feature is quantified at
  the intersection.
- The intensity of the shade corresponds to the absolute value of the
  correlation.
- We should always understand the rational for row or column ordering:
  in that case, an unsupervised hierarchical classification was applied;
  within rows (or columns) to close features (distance derived from correlation)
  will be found grouped together. The information is supported by the addition
  of the dendrogram in the margins.
- The numbers are the correlations; number by themselves may not
  be of main interest so the first visible information is actually
  the colour of the numbers corresponding to the discrimination of significance
  (yellow, p.value &lt; 0.5; green otherwise). Still, looking closer at the
  matrix give access to the actual correlation value if required (e.g. for
  reporting).
 
From that, we understand that the rows and columns features under the
magnifier glass constitute two groups which association support their
identification as good candidates to push the analysis further.

![](../../img/portfolio/heatmap.png)

[modeline]: # ( vim: set foldlevel=0 spell spelllang=en_gb: )
