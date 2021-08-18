# Phylogenetic clustering

The R script phylogenetic_clustering.R made available here performs phylogenetic partitioning/clustering using the “depth-first-search” algorithm described by Prosperi et al. This script is adapted from [here](https://www.r-bloggers.com/2012/11/finding-meaningful-clusters-in-phylogenetic-trees-or-other-hierarchical-clusterings/). A phylogenetic tree in newick format and a matrix of pairwise SNP distances are taken as input. The phylogenetic tree is then partitioned into clusters using a “depth-first-search” algorithm (1), in which the phylogenetic tree is scanned from the root and an internal node classified as a cluster if the maximum pairwise genetic distance among all its descendant isolates (i.e. tips) is less than or equal to a chosen SNP threshold (_thresh_ variable on script). The minimum bootstrap value of internal nodes when defining clusters can also be chosen (_rthresh_ variable in script).

1. Prosperi MCF, Ciccozzi M, Fanti I, et al. A novel methodology for large-scale phylogeny partition. Nat Commun. 2011;2(May):321. doi:10.1038/ncomms1325

# Prerequisites

The following R packages are needed to run the script phylogenetic_clustering.R (in brackets the package versions the script was tested with)

* BMhyd (1.2-8)
* Igraph (1.2.6)
* geiger (2.0.7)
* phangorn (2.7.1)
* ape (5.5)

# License
This script is a free software, licensed under GNU General Public License v3.0

# Feedback/Issues
Use the [issues page](https://github.com/francesccoll/phylogenetic_clustering/issues) to report on usage issues.

# Citation
If you find this script useful for your work please cite any of these two papers (for which the script was written):

Coll F, Harrison EM, Toleman MS, et al. Longitudinal genomic surveillance of MRSA in the UK reveals transmission patterns in hospitals and the community. Science Translational Medicine. 2017;9(413):eaak9745. doi:10.1126/scitranslmed.aak9745

Gouliouris T, Coll F, Ludden C, et al. Quantifying acquisition and transmission of Enterococcus faecium using genomic surveillance. Nature Microbiology. 2021;6(1):103-111. doi:10.1038/s41564-020-00806-7
