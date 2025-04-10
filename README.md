# CheatSheet

read depth<4×and (set value to 4)
a minimum thresholdmapping quality of 44 (44 value) 
positions with>40% missingdata and (not necessary, no value, as all have less than 40% missingness)
a minimum allele frequency<0.014. (.014)




In order to determine whether genetic grouping corresponds
with the geographic locations where isolates were collected, an
ML tree was reconstructed using RAxML (1,000 bootstrap
replicates; MULTIGAMMAI model of substitution) (Stamatakis
2014). 

In addition, the R packages poppr (Kamvar et al. 2014,
2015a) and adegenet (Jombart 2008) were used to perform a
DAPC (Jombart et al. 2010), retaining 100 principal components and three discriminant components among the samples
obtained from each of the geographic locations (state or province) in the study. Seven samples with no geographic information (01_02, AB0302, ONT0402D, T104, T167, T259,
and T426) were removed from the following analyses. To determine the degree of genetic differentiation among geographic
locations, we calculated a Mantel’s test (Sokal 1979) using the
mantel.rtest function at the ade4 R package (Dray and Dufour
2007), where the genetic distances calculated via bitwise distance were contrasted against the centroid of each state or
province, and pairwise Weir and Cockerham’s Fst (Weir and
Cockerham 1984) between all geographic locations sampled
using the assigner R package (Gosselin et al. 2019).
To predict the number of genetic clusters that represent the
most plausible number of genetic groups for S. musiva in the
United States and Canada, we used the find.clusters function in
adegenet, retaining 100 principal components and three discriminant components. The find.clusters function used a maximum K of 13, the same number of states or provinces from
which samples in this study were isolated. To determine the
best K model, a selection of the best K value was performed
via BIC in the find.clusters function. A DAPC was performed
across the new genetic clusters to determine the posterior
probability of each isolate membership in the predicted
cluster. These predicted-genetic clusters represented the new

populations of S. musiva in North America and were used in all
subsequent analyses.
To identify the degree of population differentiation between
the newly predicted-genetic clusters for all pairwise combinations, differentiation was calculated via Weir and Cockerham’s
Fst (Weir and Cockerham 1984) in the R package assigner
(Gosselin et al. 2019). Migrate-n was used to estimate the
mutation scaled migration rate between genetic clusters, rates
of mutation under mutation-drift equilibrium, and q among the
predicted-genetic clusters (Beerli and Felsenstein 2001).
Migrate-N used the following parameters: 1,000,000 steps with
10 replicates, one hot chain, and three cold Monte Carlo
Markov chain chains to estimate q for each predicted-genetic
cluster and migration rate between all plausible pairs of		
predicted-genetic clusters.


- how to write out a plot in R to a file (can make it pdf)

png("unfiltered.png")

{plot function}

dev.off()

- sign in

ssh -X -o ServerAliveInterval=30 -p 732 barenom@shell.cgrb.oregonstate.edu

sftp -o Port=732 barenom@files.cgrb.oregonstate.edu

- git password

[link here](https://docs.google.com/document/d/1z3_ojKPFrOTEBN-JShzeLMroCvjeOIEV5TvOIYKtCcM/edit?usp=sharing)

- git pipeline

git pull .

git add .

git commit -m "update"

git push

git pull

- submissions

SGE_Batch -c " -P 4 -q bpp@anduin -r jobname

- sftp commands

get [file] (download file from cluster to local device)

put [file] (upload file from local device to cluster)

- how to get a random subset of a vcf

bcftools view FULLVCF.vcf | vcfrandomsample -r (float object, fraction of genome maintained) > SUBSET.vcf

- 
Rscript --vanilla scipt.R

sh scrip.sh

wrapper
- scripts
- wrapper.sh
* documenting is very important here!

Rmd cheat sheet
https://www.rstudio.com/wp-content/uploads/2015/02/rmarkdown-cheatsheet.pdf



R code:
atomic vectors - one data type
list - multiple data type
paste(x, collapse=y) #y refers to what to delimit the elements in the vector by
Paste(x, sep=y) # what to put between each x
y<-x[!is.na(x)] #gives us a vector y that is a subset of 
                # x that is not NA
