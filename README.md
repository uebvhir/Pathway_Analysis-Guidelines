# UEB-Pathway Analysis 

[The Statistics and Bioinformatics Unit ([UEB](http://ueb.vhir.org))](ueb.vhir.org)  at Vall d'Hebron Research Institute (VHIR) is a support platform whose mission is providing expert advice, services and training in bioinformatics and statistics for clinical and biomedical research.

At the bioinformatics platform of [UEB](http://ueb.vhir.org) we work with distinct omics data and apply our knowledge to provide researchers with accurate. reliable, robust and, if possible, quick results.

Many of our analyses deal with selecting some type of "feature" such as genes, proteins, microRNAs etc. which may act as a biomarkers for distinguishing, predicting or classifying distinct biological states. 

These analyses can be roughly separated in two parts: 
1. Obtaining a list of features, which is usually the result applying some type of statistical or bioinformatical methods and 
2. Doing a biological interpretation of these lists using some type of *Pathway Analysis*, where the term *Pathway* or *Network Analysis* denotes any analytic technique that benefits from biological pathway or molecular network information to gain insight into a biological system. (Creixell et alt, Nature Methods 2015 (12 (7)). 


## What's this site for

This document provides guidelines and examples of the analyses that can be performed on one or more gene lists to help gain biological insight on the results of some type of omics data analysis (e.g. selection of differentially expressed genes). 

Overall these analyses are known as **Pathway Analysis**. Although one could discuss the exact meaning of the term we will keep it and from now on it will be used to describe any analysis based on a list of genes or other molecular features obtained from an omics data analysis.

There is a huge variety of methods and tools for doing pathway analysis. [Khatri (2012)](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1002375) is still a good reference to provide a good comparative overview. We refer the reader to this and similar papers and go straight to the list of recommended tools.

# Pathway Analysis

Because we do not aim so much at being comprehensive as at being useful we begin considering three possible approaches that can be undertaken by a researcher when she is faced with the mission of *"doing a pathway analysis of my gene list"* 

As the page progresses we expect to add more examples, more tools, and more explanations.

These three approaches described below differ in sophistication and in difficulty. 

1. The first and simplest one only requires providing a list of genes and going through some web pages that do some variation of *enrichment analysis*. 
2. A second one is a protocol described in a recent Nature paper that requires using a variety of programs to be completed. While "intended for biologists" it requires at least some time to learn what each tool does, how to set the parameters and how to interpret the results.
3. The last one relies on [Bioconductor](http://bioconductor.org) and R, and as such, it assumes familiarity with the use of R and [Bioconductor](http://bioconductor.org) for bioinformatic analysis.

## Use a single online tool

The simplest way to do pathway analysis consists of using one of the tools embedded in popular pathway databases such as [The Gene Ontology](www.geneontology.org) and [Reactome](www.reactome.org). Each website contains some tool to do pathway analysis.

  - The Gene Ontology ([www.geneontology.org](www.geneontology.org)) provides a form for doing *Gene Enrichment Analysis* in its front page. Just paste a list of identifiers and press "launch". Simple help is provided by pressing a "?" symbol.
  - The Reactome web site ([www.reactome.org]()) has an option to do data analysis ("Analyze Data") which allow doing a step by step enrichment analysis. Besides the examples contained in the site, one can find a short online tutorial on using this tool in the EMBL web site: [Reactome: Tools for analysis of biological pathways](https://www.ebi.ac.uk/training/online/course/reactome-tools-analysis-biological-pathways).

There are many other web pages or standalone programs that can be used to do pathway analysis. See some of them in the "Pathway Analysis Tools" section.

## Apply a pipeline (protocol)

If one wishes to do more complete or sophisticated analysis one can turn to a recently published nature protocol: [Pathway enrichment analysis and visualization of omics data using g:Profiler, GSEA, Cytoscape and EnrichmentMap](https://www.nature.com/articles/s41596-018-0103-9). This protocol shows how to use some publicly available tools for going from basic enrichment analysis to visualization of results and, what is more important, to a guided interpretation. The protocol is pay-only but a preprint is available at biorXiv: [Pathway enrichment analysis of -omics data (preprint)](https://www.biorxiv.org/content/biorxiv/early/2017/12/12/232835.full.pdf).

## The R/Bioconductor approach 

Last but not least one can always use state of the art tools available from the [Bioconductor project](http://bioconductor.org). Bioconductor contains many options for doing similar or distinct analyses. 

In order to avoid getting lost in the myriad of options a good starting point is the [Clusterprofiler package](https://www.bioconductor.org/packages/release/bioc/vignettes/clusterProfiler/inst/doc/clusterProfiler.html) which not only allows to do a variety of analysis with a homogeneous interface, but which also has an [excelent and extensive documentation](https://yulab-smu.github.io/clusterProfiler-book/).


# Useful materials

People tend to ask more questions like *where can I find a tool to do pathway analysis?* than  *How can I learn how to do pathway analysis the right way?* 
We are convinced that the right way to proceed is first answering the second question and next, the first one.

With this aim in mind, we have compiled some materials that we have found on the web -including ours- that can provide a gentle introduction to this topic, easier to do than to define.

## Courses and tutorials
* [An Introduction to Pathway Analysis](https://github.com/uebvhir/Pathway_Analysis-Guidelines/raw/master/Intro2PathwayAnalysis-LONG.pdf). A talk that was organized by the [[UEB](http://ueb.vhir.org)](http://ueb.vhir.org) at VHIR, to introduce basic concepts and free tools, after the Ingenuity Pathways software license was discontinued.
* [Bioinformatics Canada](www.bioinformatics.ca) teaches great bioinformatics courses on a yearly basis. Besides this, they make the materials of courses from previous years freely available on their web site. One of such courses is [Pathway and Network analysis of omics data]( https://bioinformatics.ca/workshops/pathway-and-network-analysis-of-omics-data/)  
* [VIB Bioinformatics Core](https://www.bits.vib.be/) is another must-stop place when looking for training materials. [Here](https://wiki.bits.vib.be/index.php/Functional_annotation_and_enrichment_analysis) are some tutorials on enrichment analysis using a variety of tools.
* A PLoS Computational Biology tutorial was presented at ISMB 2010: [Pathway Analysis of Expression Data: Deciphering Functional Building Blocks of Complex Diseases](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3102754/).
* [Materials from an old CNIO course on Functional Analysis](http://bioinfo.cnio.es/files/training/Functional_Analysis_Course/) (the web page is not available): 

## Bioconductor-based courses and tutorials

* Teaching materials about _Performing functional analysis on gene lists with R-based tools_ from the Harvard Chan Bioinformatics Core
  - [Using clusterprofiler](https://hbctraining.github.io/DGE_workshop_salmon/lessons/functional_analysis_2019.html)
  - [Using other tools](https://hbctraining.github.io/DGE_workshop/lessons/functional_analysis_other_methods.html)
* [Materials from a RNA-seq tutorial](https://bioconnector.github.io/workshops/r-rnaseq-airway.html)
* [A workflow on GSEA with clusterProfiler, from NYU Core facility](https://learn.gencore.bio.nyu.edu/rna-seq-analysis/gene-set-enrichment-analysis/)


## References

There are many references on pathway analysis of omics data. Indeed one might even think that there are *too many* papers on this topic because many of the methods or tools available seem to be minor variations of pre-existing methods or tools. 
Instead of trying to do an exhaustive list of papers we simply present a few papers which seem relevant to us. For a longer or more complete list see the references therein.

* Khatri, P., Sirota, M., & Butte, A. J. (2012). Ten Years of Pathway Analysis: Current Approaches and Outstanding Challenges. PLOS Computational Biology, 8(2), e1002375. https://doi.org/10.1371/journal.pcbi.1002375
* Emmert-Streib, F., & Glazko, G. V. (2011). Pathway analysis of expression data: deciphering functional building blocks of complex diseases. PLoS Computational Biology, 7(5), e1002053. https://doi.org/10.1371/journal.pcbi.1002053
* García-Campos, M. A., Espinal-Enríquez, J., & Hernández-Lemus, E. (2015). Pathway Analysis: State of the Art. Frontiers in Physiology, 6, 383. https://doi.org/10.3389/fphys.2015.00383
* Reimand, J., Isserlin, R., Voisin, V., Kucera, M., Tannus-Lopes, C., Rostamianfar, A., … Bader, G. D. (2017). Pathway enrichment analysis of -omics data. BioRxiv, 232835. https://doi.org/10.1101/232835


# Pathway Analysis Tools

There are literally dozens, probably hundreds of Pathway Analysis Tools. The table below contains an opinionated list of a few popular tools that cover the spectra of tools types, such as commercial/non-commercial, web based/standalone/R based.
Only one link escape from this classification: the link [https://tools4mirs.org/software/target_functional_analysis/](https://tools4mirs.org/software/target_functional_analysis/) points to a page which at its time points to functional analysis tools for microRNAs target genes.

| **Tool Name**   | **Web interface** | **Standalone** | **R version** | **Commercial** |
|-----------------|-------------------|----------------|---------------|----------------|
| [DAVID](https://david\.ncifcrf\.gov/)           | yes               | no             | yes           | no             |
| [PANTHER](http://pantherdb\.org/)         | yes               | no             | no            | no             |
| [WebGestalt]( http://www\.webgestalt\.org/)      | yes               | no             | no            | no             |
| [GSEA](http://software\.broadinstitute\.org/gsea/index\.jsp)            | no                | yes            | yes           | no             |
| [g:Profiler](https://biit\.cs\.ut\.ee/gprofiler/gost)      | yes               | no             | yes           | no             |
| [Enrichr](https://amp\.pharm\.mssm\.edu/Enrichr/)         | yes               | no             | yes           | no             |
| [Tools4miRs](https://tools4mirs\.org/software/target_functional_analysis/)      | yes               | NA             | NA            | NA             |
| [clusterprofiler](https://bioconductor\.org/packages/release/bioc/html/clusterProfiler\.html) | no                | no             | yes           | no             |
| [Pathvisio](https://www\.pathvisio\.org/)       | yes               | no             | no            | no             |
| [GeneGo/MetaCore](https://portal\.genego\.com/) | no                | yes            | no            | yes            |
| [IPA](https://www\.qiagenbioinformatics\.com/products/ingenuity\-pathway\-analysis/)             | no                | yes            | no            | yes            |


