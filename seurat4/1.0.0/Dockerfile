FROM ghhenry/r4:1.0.0
LABEL author="Gervaise H. Henry"

RUN R -e "install.packages(c(\"Seurat\"))" && \
    conda install anndata==0.6.19 scipy==1.2.1 -c bioconda && \
    R -e "BiocManager::install(c(\"LoomExperiment\", \"SingleCellExperiment\"))" && \
    R -e "devtools::install_github(\"cellgeni/sceasy\")"