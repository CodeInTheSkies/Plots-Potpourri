 ## A Potpourri of Interesting Data Analysis Plots with Brief Explanations
 
 Here I present a growing collection of carefully chosen plots that are interesting in their own right, which have been part of various analysis projects I have been handling recently.
 
 For each plot set, I include brief context and explanations.
 
 ### 1. Expressions across cancers – one gene at a time
 
![Log expressions of selected genes in cancer versus normal tissues](/plots/MageA4_vs_MageA8.png)
 
This plot shows log expressions (box and whisker plots) of selected genes in cancer versus normal tissues. Each dot represents either a healthy individual or a cancer patient depending on the group as shown. The idea behind creating this type of plot is to identify genes that are widely expressed well across multiple cancers but minimally expressed in normal tissues. Such genes can be further chosen as candidates for future drug targets to improve chemotherapy. 

The two genes chosen demonstrate the contrasting scenarios where MAGEA4 turns out to be a good choice (and hence the green check mark), whereas MAGEA8 turns out to be a bad choice since it is expressed in so many normal tissues (hence the cross mark). 

So, one final question that may be on your mind is, _"why do we need to make sure the gene is not expressed in normal tissues"?_  This is a requirement because the drugs target these genes in the sense that they try to suppress or inhibit these genes from expressing and thereby starve the cancer progression. This is the mechanism of treatment. Therefore, this criteria makes sure that the damaging side effect of chemotherapy, where normal tissues (or cells) are also killed, is kept to the minimum.

Data source: [The Cancer Genome Atlas (TCGA)](https://www.cancer.gov/about-nci/organization/ccg/research/structural-genomics/tcga) and [The Genotype-Tissue Expression (GTEx) project.](https://gtexportal.org/home/)
 
 
![Full trend overview heatmap](/plots/FullTrend_OverviewHM.png)

The above is a full overview heatmap where the gene expressions are averaged by grouping according to the normal tissue or cancer type, and then plotted as heatmaps. So, each colored box in the heatmap represents the average expression of a given gene (row) in a given group (column). Before plotting the average values are scaled (or z-scored) to obtain zero mean and unit variance. 

Further the rows are hierarchically clustered so that similar patches occur together. We can see some interesting genes as marked that can be considered to be good candidates for further study.

Below is a zoomed-in portion of the heatmap, where the gene names are visible, and the trend is clearer _(notice the clear gene group that are quite red in the cancers and quite blue in the normals)._ 
