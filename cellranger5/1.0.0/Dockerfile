FROM ghhenry/base:1.0.0
LABEL author="Gervaise H. Henry"

RUN apt-get install -y unzip alien && \
  wget 'https://files.softwaredownloads.illumina.com/e8ed3335-5201-48ff-a2bc-db4bfb792c85/bcl2fastq2-v2-20-0-linux-x86-64.zip?Expires=1621308176&Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9maWxlcy5zb2Z0d2FyZWRvd25sb2Fkcy5pbGx1bWluYS5jb20vZThlZDMzMzUtNTIwMS00OGZmLWEyYmMtZGI0YmZiNzkyYzg1L2JjbDJmYXN0cTItdjItMjAtMC1saW51eC14ODYtNjQuemlwIiwiQ29uZGl0aW9uIjp7IkRhdGVMZXNzVGhhbiI6eyJBV1M6RXBvY2hUaW1lIjoxNjIxMzA4MTc2fX19XX0_&Signature=uJGCcDtnPEz-RKrgRFJp0alKD6Ijg9uLcFLfLW13cl42RheY-LenwOI7odEAezj8pDLltRFvM6A1ptOltKS0KJgDgFxPNkPg8zlYI0JQTB~wWWtYigLhfdx9eATEoTMCsTA3n50yYneaoGQ4xkBz1ZbGbcgKbi~~0~gu3x~dvYesMqVMxPtPd1BITrwl9meYaLqxYZyTxCdosDuFOv2QK1YTKjUqTA0MYmhBKeysUYtRy8dYktvwOHAGExegnljBbxTDQM1dpxAn5oMeM2G7OUaeQ9p7wIbvALLs7EpYo3U5q3L8-aazbIDQCZ7nqV-EdtvVrDH2PrM1CpZnoSmIhA__&Key-Pair-Id=APKAJO3UYWPXK4A26FPQ' -O bcl2fastq2-v2-20-0-linux-x86-64.zip && \
  unzip bcl2fastq2-v2-20-0-linux-x86-64.zip && \
  alien -i bcl2fastq2-v2.20.0.422-Linux-x86_64.rpm && \
  rm  bcl2fastq2*

RUN cd /opt && \
  wget -O cellranger-5.0.1.tar.gz "https://cf.10xgenomics.com/releases/cell-exp/cellranger-5.0.1.tar.gz?Expires=1621351102&Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9jZi4xMHhnZW5vbWljcy5jb20vcmVsZWFzZXMvY2VsbC1leHAvY2VsbHJhbmdlci01LjAuMS50YXIuZ3oiLCJDb25kaXRpb24iOnsiRGF0ZUxlc3NUaGFuIjp7IkFXUzpFcG9jaFRpbWUiOjE2MjEzNTExMDJ9fX1dfQ__&Signature=Xnx5ppE69anV5HBNDO7jlYHpXY8ViLSLT2mr~L4AgCN52xM8aIqtDRq1xR80lrfeHr7q0pcWBCaacwHNSvhkm8bCLU4Os03skJokHT8LNH~pB3a62GRfhBvyWeq2-zcPOCtBw2GchieJLylY91g0jkjAOvMplsIm7Vk0jdXuNXPBy1--8qAEvCGOYqOf84nU5n7S23RLnoP9wBa~ys-4KdjaJll5LrIB7KFbfmKz-uRIuP6JBsl9lBOPeJxeEZIh5ziovx2NFWZKf8MPnsKje3N008ZaUHrgdO57Jyfduk-VvY0ByepBwMCJUQBCKIE~WaVMX7Yur19ZL2~XN6btfQ__&Key-Pair-Id=APKAI7S6A5RYOXBWRPDA" && \
  tar -xzvf cellranger-5.0.1.tar.gz
ENV PATH=/opt/cellranger-5.0.1:$PATH