# A microphysiological model of human trophoblast invasion during early embryo implantation
Data analysis of the proteomics of the cellular proteome for the paper by Ju Young Park et al.

# Code requirements
The code was run using [R](https://cloud.r-project.org) v.4.2.0 on [Rstudio](https://rstudio.com) v1.2.5033; running the code require:

- The installation of [Devtools](https://cran.r-project.org/web/packages/devtools/index.html)

- the package[RomicsProcessor v.1.0.0](https://github.com/PNNL-Comp-Mass-Spec/RomicsProcessor/blob/master/RomicsProcessor_1.0.0.tar.gz) (follow the package page for installation instructions). RomicsProcessor is an R package that can be used to analyze omics data. The package provides a structured R object to store the data, allowing for reproducible data analysis. The package also supports creating analytical pipelines from previously processed objects and applying these pipeline to other objects. This allows for rapid development and reuse of bioinformatics methods.

- [ProteinMinion](https://github.com/GeremyClair/Protein_MiniOn) is an R package created to retrieve annotation from different online sources (UniProt, KEGG, Reactome, etc.) and to perform enrichment analysis using popular enrichment functions including Fisher's exact tests, Hypergeometric, binomial, and KS test. 

- the package [DT](https://cran.r-project.org/web/packages/DT/index.html) was used to visualize tables. 

- To run the code create a copy of the repository in a folder on your computer and open the file named "02 - Code.Rmd" 

- The version of the different dependencies that were employed at time of analysis are contained in the "romics_proteins.rda" object located in the folder ".*/03 - Output files". After loading the object in the R enviromnemt you can get the version of all packages by typing the following in the R console
```
romics_proteins$dependencies

```

# Data pre-processing

The data was pre-processed using MaxQuant (v1.6.0.16) the file [parameters.txt](https://github.com/GeremyClair/Implantation_on_a_chip_Proteomics/blob/main/01%20-%20Source%20files/parameters.txt) generated by MaxQuant is provided. The [summary.txt](https://github.com/GeremyClair/Effect_of_glomerular_disease_on_the_podocyte_cell_cycle/blob/main/01_Source_files/summary.txt) file indicates what raw files located on MassIVE were used for the analysis. The [peptide.txt](https://github.com/GeremyClair/Effect_of_glomerular_disease_on_the_podocyte_cell_cycle/blob/main/01_Source_files/peptides.txt) and [proteinGroups.txt](https://github.com/GeremyClair/Implantation_on_a_chip_Proteomics/blob/main/01%20-%20Source%20files/proteinGroups.txt) files are also provided along with the metainformation of associated with the samples in the file [metadata.csv](https://github.com/GeremyClair/Effect_of_glomerular_disease_on_the_podocyte_cell_cycle/blob/main/01_Source_files/metadata.csv).

The [R markdown knitR report file](https://github.com/GeremyClair/Effect_of_glomerular_disease_on_the_podocyte_cell_cycle/raw/main/02_Code_cell_cycle_alport_proteomics.html) final report can be seen directly without having to run the code.

All the files generated during the data analysis are located in the folder 03 - Output files.
It is important to note that the fasta files uploaded from UniProts were the ones used for the search

Please let us know if you need any assistance in executing or understanding this code.

## Contacts

Written by @GeremyClair for the Department of Energy (PNNL, Richland, WA) \
E-mail: geremy.clair@pnnl.gov or proteomics@pnnl.gov \
Website: https://omics.pnl.gov/ or https://panomics.pnnl.gov/

## License

This code is licensed under the 2-Clause BSD License; 
you may not use this file except in compliance with the License.  You may obtain 
a copy of the License at https://opensource.org/licenses/BSD-2-Clause

Copyright 2019 Battelle Memorial Institute

