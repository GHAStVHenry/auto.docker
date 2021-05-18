FROM ghhenry/base:1.0.0
LABEL author="Gervaise H. Henry"

RUN apt-get install -y unzip alien && \
  wget 'https://files.softwaredownloads.illumina.com/e8ed3335-5201-48ff-a2bc-db4bfb792c85/bcl2fastq2-v2-20-0-linux-x86-64.zip?Expires=1621305945&Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9maWxlcy5zb2Z0d2FyZWRvd25sb2Fkcy5pbGx1bWluYS5jb20vZThlZDMzMzUtNTIwMS00OGZmLWEyYmMtZGI0YmZiNzkyYzg1L2JjbDJmYXN0cTItdjItMjAtMC1saW51eC14ODYtNjQuemlwIiwiQ29uZGl0aW9uIjp7IkRhdGVMZXNzVGhhbiI6eyJBV1M6RXBvY2hUaW1lIjoxNjIxMzA1OTQ1fX19XX0_&Signature=rfB78lCbWF0HeOqiJ5L7aQZPKn3kMYFtZi1-K1c5r79VSIxZDpQjMzCKYLjQKhVBe4V~Wk42EXI2A-2lWz5c2pIEF4F6pei~iH7QrMMCGgwtKCasCK7HrGMeT3D~1bdOIvzF8efMgzt6hn2WihL5aeIqKHjPL9ck~PvRKSmxH7HjqOsl5R-rOH~23NLnk1x8tihZQTfHMemD7DcA51sQ-kCB5tAsSIgpEOSnvXt9J1VGK-E5OUVHiFXl6HasIh~U~9dE0pM~UpfHWVuE5nX7SXx0rXU6DAuoMwFCYFTD4iYtWtfWPXZaGE1op1boI8nFg2Mh9Z3vUGM5-XcdvE9hqg__&Key-Pair-Id=APKAJO3UYWPXK4A26FPQ' -O bcl2fastq2-v2-20-0-linux-x86-64.zip && \
  unzip bcl2fastq2-v2-20-0-linux-x86-64.zip && \
  alien -i bcl2fastq2-v2-20-0-linux-x86-64.rpm && \
  rm  bcl2fastq2*

RUN cd /opt && \
  wget -O cellranger-6.0.1.tar.gz "https://cf.10xgenomics.com/releases/cell-exp/cellranger-6.0.1.tar.gz?Expires=1621348866&Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9jZi4xMHhnZW5vbWljcy5jb20vcmVsZWFzZXMvY2VsbC1leHAvY2VsbHJhbmdlci02LjAuMS50YXIuZ3oiLCJDb25kaXRpb24iOnsiRGF0ZUxlc3NUaGFuIjp7IkFXUzpFcG9jaFRpbWUiOjE2MjEzNDg4NjZ9fX1dfQ__&Signature=IvMZcvepQ4Qe64vHnrPPOVX2ekafg61uMo~jtvIZ3KmtrVUa24lU9YZFqKqSqz~wUbrYyR~eqk5A5K0OSZ05MNWN68o0qwZYM5fMVHp2hYUckUM0OiAYwIHgEe82-Gjs2QS4eJpaPtkuNq-QGK8NsZzueV~fRwLAa1hcIo8aUUCj0jHQdRM2Lopx09ZenT2taBRPaaJWuPGzZY5U08OYRYvsE~QqqvCklxy6Rg1KyERKjwOzUWFBScNd09duygu9S4~WaAdtfN6I7BpUW-Fis~hwsTN~hUTBG6EVesc0VxWhbQC3Tl66gsofvd5fq8aeqGVJk7tnfJkxIMb5oirc8Q__&Key-Pair-Id=APKAI7S6A5RYOXBWRPDA" && \
  tar -xzvf cellranger-6.0.1.tar.gz
ENV PATH=/opt/cellranger-6.0.1:$PATH