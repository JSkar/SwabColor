# SwabColor
R and Python3 Code for Swab Color Publication

DOI Link: https://doi.org/10.3389/fmicb.2024.1466375

The purpose of this code is to look for correlations between the darkness of swabs collected orally from dairy cows and the structure of the bacterial and fungal communities. We hypothesize that darker swabs are more similar to the ruminal communities than lighter swabs, due to the color being from collected rumen remnants. This code explores alpha diversity metrics, beta diversity metrics, and the ASVs (Amplicon Sequence Variants) driving difference between the light and dark swabs. We also explore how darkness affects the similarity of swabs to rumen samples collected directly from the cow rumen collected at the same time from the same farm.

Files:

physeq.zip: Bacterial Phyloseq Object. Contains ASV table, metadata, taxonomy, and phylogenetic information. Data was generated using DADA2's standard workflow.

physeq_fungal.zip: Fungal Phyloseq Object. Contains ASV table, metadata, taxonomy, and phylogenetic information. Data was generated using DADA2's standard workflow.

Cropping and Darkness Scoring.ipynb: Python3 script using OpenCV to crop a 100x100 square from the center of the swab images. We then use OpenCV to convert the images to grayscale, and convert the average darkness of the images to a 0-1 scale (White - Black).

Swab Photo Score Analysis.Rmd: R script to correlate darkness scores with alpha diversity, beta diversity, and SIMPER/Kruskal Wallis analyses.

Heatmap Generation.Rmd: R script to generate the heatmaps from the SIMPER/Kruskal Wallis analysis results.

Intersection Analysis.Rmd: R script to calculate the "Core" ASVs, and then determine how many of those core ASVs are captured by the swabs. Correlates darkness scores to those counts.
