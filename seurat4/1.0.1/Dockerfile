FROM ghhenry/r4:1.0.0
LABEL author="Gervaise H. Henry"

RUN sudo apt-get install -y libhdf5-dev && \
  R -e "install.packages(c(\"Seurat\",\"hdf5r\"))" && \
  conda install anndata==0.6.19 scipy==1.6.3 -c bioconda && \
  R -e "BiocManager::install(c(\"LoomExperiment\", \"SingleCellExperiment\"))" && \
  R -e "devtools::install_github(\"cellgeni/sceasy\")"
