# Explainable AI for Generative Design of a Pedestrian Bridge


<!-- A repository of structural information on the design of pedestrian bridges
============================== -->

![XAI_Pedestrian logo](Cover_BridgeGenomeProject.png)

- Does your data science technique actually scale across hundreds of buildings?
- Is it actually faster or more accurate?

These are questions that researchers should ask when developing data-driven methods. Building performance prediction, classi cation, and clustering algorithms are becoming an essential part of analysis for anomaly detection, control optimization, and demand response. But how do we actually compare, each individual technique against previously created methods?

The time-series data mining community identifed this problem as early as 2003: “Much of this work has very little utility because the contribution made”...“offer an amount of improvement that would have been completely dwarfed by the variance that would have been observed by testing on many real world datasets, or the variance that would have been observed by changing minor (unstated) implementation details.” ([Keogh, E. and Kasetty, S.: On the need for time series data mining benchmarks: A survey and empirical demonstration. Data Mining and Knowledge Discovery, 7(4):349–371, Oct. 2003.](https://link.springer.com/article/10.1023/A:1024988512476))

[They created the time-series data benchmarking set](http://www.cs.ucr.edu/~eamonn/time_series_data/). This data set enables testing of new techniques on an assortment of real world data sets. For commerical buildings data, we are doing the same!

## The need for Benchmarking Data Sets of Bridges for Scientific Data Analytics

### Typically bridges are designed, verified and constructed from scratch, depending on the prior knowledge of the involved team of engineers. Hence for most of the existing bridge buildings performance data are not available in digital and / or computational form for further science studies. Thus individual researchers and engineers in practice creating their own methods, finding a case study data set and determining efficacy on their own. Not surprisingly, most of those researcher find positive, yet questionably meaningful results.

![ForwardModel](https://github.com/mkrausAi/mkrausAI.github.io/blob/main/research/01_SciML/01_BH_PedestrianBridge_XAI/Forward_Model_UserInterface.mp4)


### Using a large, consistent benchmark data set from hundreds (or thousands) of buildings, a researcher can determine how well their methods actually perform across a heterogeneous data set. If multiple researcher use the same data set, then there can be meaningful comparisons of accuracy, speed and ease-of-use.

![InverseModel](https://github.com/mkrausAi/mkrausAI.github.io/blob/main/research/01_SciML/01_BH_PedestrianBridge_XAI/Inverse_Model_UserInterface.mp4)

## Introducing the Building Data Genome Project
It is an open data set from 507 non-residential buildings that includes hourly whole building electrical meter data for one year. Each of the buildings has meta data such as  or area, weather, and primary use type. This data set can be used to benchmark various statistical learning algorithms and other data science techniques. It can also be used simply as a teaching or learning tool to practice dealing with measured performance data from large numbers of non-residential buildings. The charts below illustrate the breakdown of the buildings according to location, building industry, sub-industry, and primary use type.

![meta data](https://github.com/mkrausAi/mkrausAI.github.io/tree/main/research/01_SciML/01_BH_PedestrianBridge_XAI/DataSet)

### Please contribute new data sets or provide analysis examples in Jupyter or R markdown using the data


Citation of Data-Set
------------

[xxx](http://www.sciencedirect.com/science/article/pii/S1876610217330047) 

[ResearchGate](https://ww)

```
BibTex:
@article{xxx,
title = "xxx ",
journal = "xx"
}
```

# Contact
Dr. Michael A. Kraus, M.Sc.(hons)
Institute für Baustatik und Konstruktion (IBK)
ETH Zürich
kraus@ibk.baug.ethz.ch
https://kaufmann.ibk.ethz.ch/de/personen/mitarbeitende/dr-michael-anton-kraus.html

------------
The MIT License (MIT)
Copyright (c) 2022, Vera Balmer, Rafael Bischof, Sophia Kuhn and Michael Kraus

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

