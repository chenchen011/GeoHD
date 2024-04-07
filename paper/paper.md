---
title: 'GeoHD: A Python toolkit for geospatial hotspot detection, visualization, and analysis'
tags:
  - Python
  - GIS
  - hotspot detection
  - visualization
  - geographic analysis
authors:
  - name: Yuchen Yan^[Corresponding author]
    orcid: 0000-0002-0245-2241
    equal-contrib: true
    affiliation: "1" 
- name: Yuxin Wang
   orcid: 0009-0004-7063-3935
   affiliation: "1"
affiliations:
 - name: School of Transportation Science and Engineering, Harbin Institute of Technology, China
   index: 1
date: 10 April 2024
bibliography: paper.bib

---

# Summary

In the field of urban data analysis, the spatial distribution of research objects often exhibits non-uniformity, characterized by distinct spatial heterogeneity. Areas with higher densities of point data often signify hotspots of events within those regions. Consequently, detecting hotspots within urban areas has become a focal point in urban research, holding significant value for urban planners, researchers, and management authorities. Taking crime hotspot detection as an example, analyzing historical crime data can unveil the underlying causes of criminal activities, thereby aiding relevant management authorities in formulating more effective crime prevention strategies. In past research, various classical clustering algorithms or hotspot analysis methods such as Getis-Ord spatial statistics, k-means clustering, and kernel density analysis have been applied to urban hotspot detection. Furthermore, tailored hotspot detection approaches have been proposed by scholars for specific research contexts such as transportation, traffic accidents, and crime. Despite the emergence of excellent context-specific hotspot visualization tools like transbigdata based on transportation, challenges persist in current hotspot detection research. Existing studies often remain confined to singular research contexts, lacking comprehensive hotspot detection analysis frameworks. Additionally, current geographic processing tools primarily focus on heatmap visualization, impeding precise hotspot localization. Given the complexity of geographic spatial data, researchers from different backgrounds may encounter operational difficulties, exacerbated by the considerable learning curve associated with prevalent geographic information system software like ArcGIS. Hence, there is an urgent need to develop a universally applicable and user-friendly open-source hotspot detection tool to meet the diverse analytical needs of researchers in urban hotspot analysis.

# Statement of need

GeoHD is a Python toolbox designed for the detection, visualization, and analysis of geographical spatial hotspots. Its primary objective is to provide a user-friendly tool applicable across various urban research backgrounds for hotspot detection and analysis. The working principle of GeoHD is illustrated in Figure 1. Initially, GeoHD conducts clear visualization and statistical analysis on input data to obtain Kernel Density Estimation (KDE) results. Subsequently, it employs a window analysis method to compute the maximum value surface of raster data pixels, followed by performing algebraic subtraction between the density field surface and the maximum value surface to obtain the difference result, i.e., the non-negative value surface. At this stage, positions with zero values in the difference result within each window represent the locations of local hotspots in the current area. After completing the window analysis, a reclassification algorithm is utilized to classify extreme value areas and areas excluding extreme values into two categories. Ultimately, the extreme value areas obtained through this process represent the hotspots of events occurring within the current area.

Currently, GeoHD primarily includes the following functionalities:

* Visualization of the true distribution of research data: Enables visualization of the true geographical spatial positions of point data by inputting point data.

* Kernel density analysis with fixed bandwidth and adaptive bandwidth: Implements classic fixed bandwidth kernel density estimation and optimized adaptive bandwidth kernel density estimation, providing adjustable parameters and clear visualization.

* Geographical spatial hotspot detection based on fixed bandwidth and adaptive bandwidth: Extracts local research hotspots by combining density analysis and raster algebra, ultimately obtaining hotspot detection results.

* Point pattern analysis: Provides functionality for plotting Ripley G, Ripley F, Ripley J, Ripley K, and Ripley L functions for hotspot distribution.

* Hotspot analysis using rectangular  grids and hexagonal grids: Implements statistical analysis of spatial point data based on matrix grids and hexagonal grids, providing clear visualization.

The development of GeoHD fills the gap in universality and usability of current hotspot detection tools, offering a comprehensive and effective analysis tool for the urban research field. For the latest version of GeoHD and usage instructions, please refer to the following link: https://github.com/yan-yuchen/GeoHD.

# Use Case




# Citations

Citations to entries in paper.bib should be in
[rMarkdown](http://rmarkdown.rstudio.com/authoring_bibliographies_and_citations.html)
format.

If you want to cite a software repository URL (e.g. something on GitHub without a preferred
citation) then you can do it with the example BibTeX entry below for @fidgit.

For a quick reference, the following citation commands can be used:
- `@author:2001`  ->  "Author et al. (2001)"
- `[@author:2001]` -> "(Author et al., 2001)"
- `[@author1:2001; @author2:2001]` -> "(Author1 et al., 2001; Author2 et al., 2002)"

# Figures

Figures can be included like this:
![Caption for example figure.\label{fig:example}](figure.png)
and referenced from text using \autoref{fig:example}.

Figure sizes can be customized by adding an optional second parameter:
![Caption for example figure.](figure.png){ width=20% }

# Acknowledgements

We would like to acknowledge the comments and insights from the editors and reviewers that helped lift the quality of the project and article.

# References