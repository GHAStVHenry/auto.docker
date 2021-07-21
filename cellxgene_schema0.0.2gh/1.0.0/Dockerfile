FROM ghhenry/python3:1.0.0
LABEL author="Gervaise H. Henry"

RUN git clone https://github.com/GHAStVHenry/single-cell-curation.git && \
    cd single-cell-curation && \
    git checkout GHH && \
    make install &&\
    cp ./cellxgene_schema_cli/cellxgene_schema/hgnc_complete_set.txt.gz /usr/local/lib/python3.8/dist-packages/cellxgene_schema/hgnc_complete_set.txt.gz
    