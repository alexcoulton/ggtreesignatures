<!-- README.md is generated from README.Rmd. Please edit that file -->

# ggtreesignatures

Modified version of ggtree to allow plotting of of phylogenetic trees that incorporate mutational signature information.

<!--
![example tree](img/example_tree.png)

The proportion of each cluster of mutations that is caused by a particular mutational signature is indicated by the proportion of the edge that 
is occupied by a particular colour. In the example, we can see that the first internal node is 
-->


This package adds a new option to the layout argument of the ggtree function: `signatures`. If the `signatures` layout is used, an additional argument, `signature.df`,
must be supplied to the `ggtree` function.

`signature.df` accepts a data frame with 3 columns:
- `node`: character vector, cluster names matching the names of clusters given in the Newick tree
- `signature`: character vector, name of mutational signature
- `percentage`: numeric vector, the percentage of the cluster caused by a particular mutational signature
    
    
Each row in this dataframe corresponds to a single signature in a single cluster. The percentages of rows corresponding to a single cluster should sum to 100.


# Install

```
library(devtools)
install_github('alexcoulton/ggtreesignatures')
```





ggtree: an R package for visualization of phylogenetic trees with their annotation data
=======================================================================================

<a href="https://yulab-smu.github.io/treedata-book/"><img src="https://raw.githubusercontent.com/Bioconductor/BiocStickers/master/ggtree/ggtree.png" height="200" align="right" /></a>

[![platform](http://www.bioconductor.org/shields/availability/devel/ggtree.svg)](https://www.bioconductor.org/packages/devel/bioc/html/ggtree.html#archives)
[![](https://img.shields.io/badge/release%20version-2.4.1-green.svg)](https://www.bioconductor.org/packages/ggtree)
[![codecov](https://codecov.io/gh/GuangchuangYu/ggtree/branch/master/graph/badge.svg)](https://codecov.io/gh/GuangchuangYu/ggtree)
[![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://awesome-r.com/#awesome-r-graphic-displays)

<!--
[![Project Status: Active - The project has reached a stable, usable state and is being actively developed.](http://www.repostatus.org/badges/latest/active.svg)](http://www.repostatus.org/#active)
[![Bioc](http://www.bioconductor.org/shields/years-in-bioc/ggtree.svg)](https://www.bioconductor.org/packages/devel/bioc/html/ggtree.html#since)
[![Last-changedate](https://img.shields.io/badge/last%20change-2021--01--08-green.svg)](https://github.com/GuangchuangYu/ggtree/commits/master)

` r badge_devel("guangchuangyu/ggtree", "green")`
` r badge_bioc_download("ggtree", "total", "blue")`
` r badge_bioc_download("ggtree", "month", "blue")`
` r badge_bioc_download_rank("ggtree")`
-->

‘ggtree’ extends the ‘ggplot2’ plotting system which implemented the
grammar of graphics. ‘ggtree’ is designed for visualization and
annotation of phylogenetic trees and other tree-like structures with
their annotation data.

For details, please visit
<a href="https://yulab-smu.top/treedata-book/" class="uri">https://yulab-smu.top/treedata-book/</a>.

:writing\_hand: Authors
-----------------------

Guangchuang YU

School of Basic Medical Sciences, Southern Medical University

<a href="https://guangchuangyu.github.io" class="uri">https://guangchuangyu.github.io</a>

[![Twitter](https://img.shields.io/twitter/url/http/shields.io.svg?style=social&logo=twitter)](https://twitter.com/intent/tweet?hashtags=ggtree&url=http://onlinelibrary.wiley.com/doi/10.1111/2041-210X.12628/abstract&screen_name=guangchuangyu)
[![saythanks](https://img.shields.io/badge/say-thanks-ff69b4.svg)](https://saythanks.io/to/GuangchuangYu)
[![](https://img.shields.io/badge/follow%20me%20on-WeChat-green.svg)](https://guangchuangyu.github.io/blog_images/biobabble.jpg)

If you use [ggtree](http://bioconductor.org/packages/ggtree) in
published research, please cite the most appropriate paper(s) from this
list:

1.  **G Yu**. Using ggtree to visualize data on tree-like structures.
    ***Current Protocols in Bioinformatics***, 2020, 69:e96. doi:
    [10.1002/cpbi.96](https://doi.org/10.1002/cpbi.96).
    -   [Source code and data to reproduce figures in the
        article](https://github.com/GuangchuangYu/ggtree-current-protocols)
2.  **G Yu**<sup>\*</sup>, TTY Lam, H Zhu, Y Guan<sup>\*</sup>. Two
    methods for mapping and visualizing associated data on phylogeny
    using ggtree. ***Molecular Biology and Evolution***, 2018,
    35(2):3041-3043. doi:
    [10.1093/molbev/msy194](https://doi.org/10.1093/molbev/msy194).
    -   [Source code to produce Supplementary
        Material](https://github.com/GuangchuangYu/plotting_tree_with_data)
3.  **G Yu**, DK Smith, H Zhu, Y Guan, TTY Lam<sup>\*</sup>. ggtree: an
    R package for visualization and annotation of phylogenetic trees
    with their covariates and other associated data. ***Methods in
    Ecology and Evolution***. 2017, 8(1):28-36. doi:
    [10.1111/2041-210X.12628](https://doi.org/10.1111/2041-210X.12628).

:sparkling\_heart: Contributing
-------------------------------

We welcome any contributions! By participating in this project you agree
to abide by the terms outlined in the [Contributor Code of
Conduct](CONDUCT.md).
