
# To do list:
## High Priority
Bioconductor analyses (R)

Download and run either Mirge or BCBio sRNA analysis for an alga

Biopython or biotite (Python)

sRNA visualisation package (isomirs, tissue-specific expression, etc)

Genome visualisation figure - genome size, ploidy, chromosome number, Phylogeny (?) all combined into 1 for key crops, livestock, and models
https://www.ncbi.nlm.nih.gov/books/NBK21120/
https://en.wikipedia.org/wiki/Genome_size
https://www.frontiersin.org/articles/10.3389/fmicb.2021.761869/full
https://onlinelibrary.wiley.com/doi/full/10.1002/ece3.7222
https://en.wikipedia.org/wiki/Pan-genome


## Semi-ideas:
Use alphafold APIs (see paper in mendeley comp tools) to make python script to download protein structures from list of accessions
Bonus to this - see if alphafold has the accession. If so download. If not, ncbi blast API to find relatives. Take top X and search alphafold for those.

Use python to regex for specific molecules in genome scale metabolic models

Crop price visualisation dashboard from WFP data
https://glomip.cgiar.org/ - portal for rice product data - how to summarise this?

Learn GWAS
  If data from Microbiome homeostasis on rice leaves is regulated by a precursor molecule of lignin biosynthesis is available, this would be cool and has a link to metabolomics as well

Visualise features of different sequencing technologies (and cartoons of how they work)
https://www.genengnews.com/topics/omics/what-will-2024-mean-for-ngs-and-genomics/

Visualisation of N application for UK crops - https://www.sruc.ac.uk/media/eeelqian/tn731-nitrogen-recommendations-for-cereals-oilseed-rape-and-potatoes-update-31-10-2022.pdf

Reference graph showing crop yields, calories, nutrients per Ha (average), with years of intense research effort

Something with ref quality genomes - https://www.nature.com/articles/s41587-023-02100-3.epdf?sharing_token=siJsl5G1GtZx4CdbXPlJq9RgN0jAjWel9jnR3ZoTv0NY_ubIAUOuSIaplQO7PxPxVH9EsfZr8kDlIzllKz52RE6fKpGkDeL1iR74azGiVtbsSEzE82YzsruF0faIgofWINM7LDgh-EVE9Yak6YVPiDe1s04ghb55P6ZIMrIXsbs%3D

Reference dashboard/interactive for selection genes - pick gene, then see what organisms, what types of selective agent they work on, etc.

http://tolweb.org/tree/home.pages/aboutoverview.html - check bottom of page for attempts to visualise the tree of life

DE example for RNA-seq data

DoE example

Get data of post office prosecutions, and amount stolen, age, race.

Conway's game of life
  Then - with evolving rules?


## Requests etc
Make stack overflow request to understand abline issue on log scale in ggplot

#TURN THE BELOW TO STACK EXCHANGE QUESTIONS------------------------------------
#Add murder rate as line
# murders %>%
#   ggplot(aes(population, total, label = abb)) +
#   geom_point(aes(color = region), size = 3) +
#   geom_text(nudge_y = 0.1) +
#   theme_minimal()  +
#   labs(title = "US gun murders in 2010") +
#   xlim(0, NA) +
#   ylim(0, NA) +
#   geom_abline(slope=r, intercept=0, lty=2, color="black") 
# #FIXED - key thing was making sure origin is plotted using xlim
# #however this also removes the log scale
# 
# #Also tried putting axes on log scale and changing intercept to 
# #small (non-zero) number 0.0001, but this didn't work
# murders %>%
#   ggplot(aes(population, total, label = abb)) +
#   geom_point(aes(color = region), size = 3) +
#   geom_text(nudge_y = 0.1) +
#   theme_minimal()  +
#   geom_abline(slope=r, intercept=0.0001, lty=2, color="black") +
#   labs(title = "US gun murders in 2010") +
#   scale_x_log10() +
#   scale_y_log10() 
# 
# # The below works, by transforming the co-ordinates instead!!!
# #Seems to relate to this (unresolved) 
# # bug https://github.com/tidyverse/ggplot2/issues/46
# murders %>%
#   ggplot(aes(population, total, label = abb)) +
#   geom_point(aes(color = region), size = 3) +
#   geom_text(nudge_y = 0.1) +
#   theme_minimal()  +
#   geom_abline(slope=r, intercept=0.0001, lty=2, color="black") +
#   labs(title = "US gun murders in 2010") +
#   coord_trans(y="log10", x="log10")
